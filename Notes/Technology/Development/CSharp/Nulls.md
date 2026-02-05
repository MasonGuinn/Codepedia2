# Notes
## 1. Fundamentals: The Concept of "Nothing"

Before writing code, we must understand what `null` actually represents in the computer's memory.

### The Memory Model: References vs. Values

To understand `null`, you must understand the difference between **Value Types** and **Reference Types**.

- **Value Types** (`int`, `bool`, `double`, `struct`):
    - Think of these as a **Box** :LiBox:.
    - The variable holds the actual data.
    - **Rule:** A box cannot be "non-existent." An `int` must always be a number (default is 0). It cannot be `null`.
- **Reference Types (`class`, `string`, `interface`, `array`)**:
    - Think of these as a **Piece of Paper with an Address** :paper.
    - The variable holds the _address_ (pointer) to where the data lives in memory (the Heap).
    - **Rule:** The piece of paper can be blank. It points to _nothing_. This state is `null`.

> [!INFO] Definition
> 
> **Null** is a literal that represents a reference that does not point to any object. It is the absence of a value.

### The Billion Dollar Mistake

Accessing a member on a `null` reference results in a runtime crash: `System.NullReferenceException` (NRE).


```cs
string name = null; // The paper is blank
int len = name.Length; // CRASH! You can't measure the length of nothing.
```

---

## 2. The Philosophy: Why, When, How

### Why do we have nulls?

We need a way to represent the **absence of information**.

1. **Uninitialized State:** A variable exists, but we haven't given it data yet.
2. **Optional Data:** A user might have a `MiddleName`, or they might not.
3. **Missing Data:** A database query for "User ID 99" might return nothing if ID 99 doesn't exist.

### When should you use nulls?

- **DO use null** for "passive" data objects (DTOs) where a field is genuinely optional (e.g., `spouse_name` for a single person).
- **DO use null** for database interactions (SQL `NULL` maps to C# `null`).
- **AVOID null** for collections. Return an empty list `new List<string>()` instead of `null`. This prevents the caller from crashing when they try to loop over it.

### How do we handle nulls?

Historically, we used "Defensive Coding":

```cs
if (variable != null)
{
    // Do something
}
```

Modern C# offers much better tools (see the Cheat Sheet below).

---

## 3. Nullable Value Types (`T?`)

Since Value Types (like `int`) can't normally be null, C# provides a wrapper called `Nullable<T>` to solve this. This is crucial for databases (e.g., an optional integer column).

### Syntax

```cs
// Long form (Under the hood)
Nullable<int> age = null;

// Short form (Syntactic Sugar - Use this!)
int? age = null;
```

### How to use them

`int?` is a struct with two helpful properties: `.HasValue` and `.Value`.

```cs
double? bankBalance = null;

// The Safe Check
if (bankBalance.HasValue)
{
    Console.WriteLine(bankBalance.Value);
}
else
{
    Console.WriteLine("Account not found.");
}

// The Safe Retrieval
// If null, return 0.0, otherwise return the value.
double finalBalance = bankBalance.GetValueOrDefault(0.0); 
```

---

## 4. Operator Cheat Sheet

C# has evolved to make handling nulls concise. Avoid deep `if/else` nesting ("Arrow Code") by using these operators.

| **Symbol** | **Name**                  | **Description**                                         | **Example**                  |
| ---------- | ------------------------- | ------------------------------------------------------- | ---------------------------- |
| **`?.`**   | **Null-Conditional**      | "If not null, go right. If null, stop and return null." | `var len = text?.Length;`    |
| **`??`**   | **Null-Coalescing**       | "If left is null, use the right side." (Defaulting)     | `var s = name ?? "Unknown";` |
| **`??=`**  | **Coalescing Assignment** | "If variable is null, assign this value to it."         | `list ??= new List<int>();`  |
| **`?[]`**  | **Null Index**            | Safely access an array or list index.                   | `var item = myList?[0];`     |
| **`!`**    | **Null-Forgiving**        | "Shut up, compiler. I know this isn't null."            | `var s = item!.ToString();`  |

### Examples in Context

#### Null-Conditional Operator (`?.`)

Commonly used to chain property access safely.

```cs
// Old way
string city = null;
if (person != null && person.Address != null)
{
    city = person.Address.City;
}

// New way
// If person is null OR Address is null, city becomes null. No crash.
string? city = person?.Address?.City;
```

#### The Coalescing Operator (`??`)

Commonly used for fallbacks/defaults.

```cs
string? input = GetUserInput();

// If input is null, use "Guest".
string username = input ?? "Guest"; 
```

#### Coalescing Assignment Operator (`??=`)

_Added in C# 8.0._ This is extremely useful for "Lazy Loading" or ensuring a variable has a value before using it.

```cs
List<int>? numbers = null;

// Old way
if (numbers == null)
{
    numbers = new List<int>();
}
numbers.Add(1);

// New way
// "If numbers is null, assign a new list to it. Then add 1."
numbers ??= new List<int>();
numbers.Add(1);
```

#### Null Index Operator (`?[]`)

Used when the **collection itself** might be null.

> [!WARNING] Important Distinction `?[]` checks if the _List_ exists. It does **not** check if the index exists. If the list is not null, but is empty, `list?[0]` will still throw an `IndexOutOfRangeException`.

```cs
string[]? tags = null;

// Returns null immediately because 'tags' is null. 
// No crash.
string? firstTag = tags?[0]; 

// Real world use: Safely invoking a delegate/event
// Only Invoke if PropertyChanged is not null
PropertyChanged?.Invoke(this, args);
```

#### Null-Forgiving Operator (`!`)

Also known as the "Dammit" operator. This does nothing at runtime; it is purely a message to the compiler to suppress warnings. Use this sparingly!

```cs
string? inputs = GetConfig(); 

// Scenario: You know 'inputs' is not null because you just validated it 
// in a way the compiler can't see (e.g., via an external file check).

if (CheckFileExists()) 
{
    // Without '!', compiler warns: "inputs might be null".
    // With '!', you say: "Trust me, I know what I'm doing."
    string validString = inputs!; 
    Console.WriteLine(validString.Length);
}
```

---

## 5. Modern Era: Nullable Reference Types (NRT)

**Crucial Context:** In C# 8.0 (released 2019), Microsoft changed the game. Before this, `string` meant "String, maybe null". Now, we can be explicit.

To use this, your `.csproj` file must have:

`<Nullable>enable</Nullable>` (Standard in .NET 6+).

### The New Mental Model

|**Type Declaration**|**Old Meaning (Pre-C# 8)**|**New Meaning (C# 8+)**|**Risk Level**|
|---|---|---|---|
|`string text`|Might be null|**Cannot** be null|Safe ✅|
|`string? text`|Same syntax didn't exist|**Might** be null|Risky ⚠️|

### Compiler Static Analysis

The compiler now reads your code flow. It warns you **before** you run the app.

```cs
public void ProcessMessage(string? message)
{
    // WARNING: 'message' may be null here.
    // Console.WriteLine(message.Length); 

    if (message != null)
    {
        // Compiler Analysis:
        // Code reachable here guarantees message is not null.
        // SAFE: No warning.
        Console.WriteLine(message.Length); 
    }
}
```

> [!WARNING] Important Note
> 
> NRTs are a **compile-time** feature. They do not change the compiled IL code. At runtime, `string` and `string?` are identical. The protections exist only to help you write better code while typing.

---
## 6. Advanced: Attributes and Generics

When writing complex libraries or helpers, the compiler sometimes gets confused. We can help it with Attributes from `System.Diagnostics.CodeAnalysis`.

### `[NotNullWhen]`

Useful for validation methods. It tells the compiler: "If this method returns true, the output parameter is definitely not null."

```cs
public bool TryGetUsername(int id, [NotNullWhen(true)] out string? name)
{
    if (id == 1)
    {
        name = "Alice";
        return true;
    }
    name = null;
    return false;
}

// Usage
string? uName;
if (TryGetUsername(1, out uName))
{
    // Compiler knows uName is NOT null here because we entered the 'if'.
    Console.WriteLine(uName.Length);
}
```

### `[MemberNotNull]`

Useful for Constructors or Initialization methods.

```cs
public class UserProfile
{
    public string Name { get; set; }

    public UserProfile()
    {
        // If we didn't call Init(),
        // the compiler would warn that 'Name' is null.
        Init();
    }

    [MemberNotNull(nameof(Name))]
    private void Init()
    {
        Name = "New User";
    }
}
```

---

## 7. The "Null Object" Pattern

Sometimes, the best way to handle nulls is to not use them at all. This is a design pattern called the **Null Object Pattern**.

Instead of returning `null`, return a "stub" object that implements the interface but does nothing.

```cs
public interface ILog {
	void Write(string msg); 
}

public class ConsoleLog : ILog 
{
    public void Write(string msg) => Console.WriteLine(msg);
}

// The Null Object
public class NullLog : ILog
{
    public void Write(string msg) 
    { 
        // Do nothing! 
    }
}

// Usage
ILog myLogger = GetLogger() ?? new NullLog();
// We never have to check "if (myLogger != null)" again.
myLogger.Write("System starting"); 
```

---

## Summary Table: Evolution of Null

| **Era**          | **Strategy**      | **Key syntax**                           |
| ---------------- | ----------------- | ---------------------------------------- |
| **C# 1.0 - 5.0** | Defensive Coding  | `if (x != null)`                         |
| **C# 6.0 - 7.0** | Syntactic Sugar   | `?.` `??`                                |
| **C# 8.0+**      | Type Safety (NRT) | `string?` vs `string`, `!`               |
| **C# 10+**       | Argument Checking | `ArgumentNullException.ThrowIfNull(val)` |

> [!TIP] Final Advice
> 
> **"Make invalid states unrepresentable."**
> 
> Try to design your classes so they _cannot_ be null. Initialize properties in the constructor. Use `null` only when "nothing" is a valid, expected answer.


# Flashcards
```flashy
What exception is thrown when you try to access a member (like .Length) on a null variable?
=System.NullReferenceException
System.ArgumentNullException
System.InvalidOperationException
System.StackOverflowException
---
In the C# memory model, which type of variable holds a pointer to an address (which can be null)?
=Reference Type
Value Type
Struct
Enum
---
To make a Value Type (like int or bool) capable of being null, you must wrap it in which struct?
=Nullable<T>
Object<T>
Optional<T>
Reference<T>
---
The short-hand syntax `int?` is syntactic sugar for {{Nullable<int>}}.
---
Which operator represents the "Null-Conditional" (Elvis) operator?
=`?.`
`??`
`??=`
`!`
---
What does the `??` (Null-Coalescing) operator do?
=Returns the left operand if not null; otherwise returns the right operand.
Assigns the right operand to the left only if the left is null.
Suppresses compiler warnings about nulls.
Accesses a member safely without throwing an exception.
---
Which operator allows you to assign a value to a variable ONLY if that variable is currently null?
=`??=`
`??`
`?.`
`?=`
---
The {{Null-Forgiving}} operator (`!`) tells the compiler to suppress null warnings because you know the value is valid.
---
In C# 8.0+ with `<Nullable>enable</Nullable>`, what does the declaration `string name;` imply?
=The variable cannot be null (Non-nullable).
The variable might be null (Nullable).
It is a compile-time error.
---
In Modern C# (NRT), how do you explicitly declare a string that IS allowed to be null?
=`string? name;`
`string name;`
`Nullable<string> name;`
`string! name;`
---
What property do you check on a `Nullable<int>` to see if it actually holds data?
=.HasValue
.IsNull
.Exist
.Value
---
This attribute is used on helper methods to tell the compiler: "If this method returns true, the out parameter is definitely not null."
===[NotNullWhen(true)]
---
The {{Null Object}} Pattern involves returning a "stub" class that does nothing, rather than returning null, to avoid null checks.
```
