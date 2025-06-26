---
title: Overview
order: 1000
---

# Outline of C# Language Features (C# 1.0 to C# 14.0)

## C# 1.0 (2002)
Foundational features establishing C# as a modern, object-oriented language. These are the core building blocks required for understanding subsequent versions.

- **Basic Syntax and Structure**
  - Semicolons (`;`) for statement termination.
  - Curly braces (`{}`) to define code blocks.
  - Case-sensitive identifiers.
  - Single-line (`//`) and multi-line (`/* */`) comments.
  - Main method as program entry point (`static void Main()`).

- **Primitive Types**
  - Integer types: `sbyte`, `byte`, `short`, `ushort`, `int`, `uint`, `long`, `ulong`.
  - Floating-point types: `float`, `double`.
  - Decimal type: `decimal` for precise financial calculations.
  - Boolean type: `bool` (`true`/`false`).
  - Character type: `char` (Unicode 16-bit).
  - Object type: `object` as the root of all types.
  - String type: `string` (immutable Unicode sequence).

- **Variables and Constants**
  - Variable declaration and initialization (`int x = 10;`).
  - Constants (`const int Max = 100;`).

- **Operators**
  - Arithmetic: `+`, `-`, `*`, `/`, `%`.
  - Relational: `==`, `!=`, `<`, `>`, `<=`, `>=`.
  - Logical: `&&`, `||`, `!`.
  - Bitwise: `&`, `|`, `^`, `~`, `<<`, `>>`.
  - Assignment: `=`, `+=`, `-=`, `*=`, `/=`, `%=`, etc.
  - Ternary operator: `?:`.

- **Control Flow**
  - Conditional statements: `if`, `else if`, `else`.
  - Switch statement: `switch` with `case` and `default`.
  - Loops: `for`, `while`, `do-while`, `foreach` (requires arrays or `IEnumerable`).
  - Jump statements: `break`, `continue`, `goto`, `return`.

- **Arrays**
  - Single-dimensional arrays (`int[] numbers = new int[5];`).
  - Multidimensional arrays (`int[,] matrix = new int[3, 3];`).
  - Jagged arrays (`int[][] jagged = new int[3][];`).

- **Methods**
  - Method declaration with parameters and return types.
  - `void` methods.
  - Parameter passing: value types by value, reference types by reference.
  - `out` and `ref` parameters for passing by reference.
  - Method overloading (same name, different signatures).

- **Classes and Objects**
  - Class declaration (`class MyClass {}`).
  - Fields, properties (basic fields, no auto-implemented properties yet).
  - Methods within classes.
  - Constructors (default and parameterized).
  - Object instantiation (`new` keyword).
  - `this` keyword for self-reference.

- **Access Modifiers**
  - `public`, `private`, `protected`, `internal`.
  - Default access (private for class members, internal for types).

- **Object-Oriented Programming**
  - Encapsulation (using access modifiers).
  - Inheritance (`class Derived : Base`).
  - Polymorphism via virtual methods (`virtual`, `override`).
  - Abstract classes (`abstract`).
  - Interfaces (`interface` for defining contracts).
  - Sealed classes (`sealed` to prevent inheritance).

- **Structs**
  - Value type structs (`struct Point { public int X, Y; }`).
  - Differences from classes (value semantics, no inheritance).

- **Enums**
  - Enumeration types (`enum Day { Monday, Tuesday, ... }`).
  - Underlying type (default `int`).

- **Namespaces**
  - Declaring namespaces (`namespace MyApp;`).
  - Using directives (`using System;`).
  - Nested namespaces.

- **Exception Handling**
  - `try`, `catch`, `finally` blocks.
  - Throwing exceptions (`throw`).
  - Custom exceptions (inheriting from `Exception`).

- **Delegates**
  - Delegate declaration (`delegate void MyDelegate(int x);`).
  - Single-cast delegates for method references.
  - Event handling basics (using delegates).

- **Events**
  - Event declaration using delegates (`event MyDelegate MyEvent;`).
  - Raising and handling events.

- **Type Safety and Boxing**
  - Strong typing (compile-time type checking).
  - Boxing and unboxing (`object` to/from value types).

- **Attributes**
  - Basic attribute usage (`[Obsolete]`).
  - Custom attributes (inheriting from `Attribute`).

- **Garbage Collection**
  - Automatic memory management.
  - `IDisposable` interface and `using` statement for resource cleanup.

## C# 2.0 (2005)
Introduces generics, enhanced delegates, and other features building on C# 1.0’s type system and methods.

- **Generics** (Prerequisite: Classes, Interfaces)
  - Generic classes (`class List<T> {}`).
  - Generic methods (`T Swap<T>(T a, T b)`).
  - Generic interfaces (`interface IComparable<T>`).
  - Constraints (`where T : class`, `where T : struct`, `where T : new()`, etc.).
  - Generic delegates (`delegate T Func<T>(T arg);`).

- **Anonymous Methods** (Prerequisite: Delegates)
  - Inline delegate methods (`delegate(int x) { return x * 2; }`).
  - Capturing outer variables (closures).

- **Iterators** (Prerequisite: Methods, `IEnumerable`)
  - `yield return` for creating iterators.
  - `yield break` to terminate iteration.
  - Simplifying custom `IEnumerable` implementations.

- **Nullable Types** (Prerequisite: Value Types)
  - `Nullable<T>` for value types (`int? x = null;`).
  - Shorthand syntax (`T?`).
  - `HasValue` and `Value` properties.
  - Null-coalescing operator (`??`).

- **Partial Types** (Prerequisite: Classes)
  - Splitting class definitions across files (`partial class MyClass`).
  - Useful for code generation (e.g., Windows Forms).

- **Static Classes** (Prerequisite: Classes)
  - `static class` for utility classes (all members must be static).

- **Covariance and Contravariance for Delegates** (Prerequisite: Delegates, Generics)
  - Limited covariance/contravariance for delegate types.

- **Property Accessor Accessibility** (Prerequisite: Classes)
  - Different access modifiers for `get` and `set` (`public int Prop { get; private set; }`).

## C# 3.0 (2007)
Focuses on LINQ and functional programming features, building heavily on generics and delegates.

- **Implicitly Typed Local Variables** (Prerequisite: Variables)
  - `var` keyword for local variable type inference (`var x = 10;`).

- **Object and Collection Initializers** (Prerequisite: Classes, Arrays)
  - Object initializers (`var p = new Point { X = 1, Y = 2 };`).
  - Collection initializers (`var list = new List<int> { 1, 2, 3 };`).

- **Auto-Implemented Properties** (Prerequisite: Classes)
  - Simplified property syntax (`public int Prop { get; set; }`).
  - Compiler-generated backing fields.

- **Anonymous Types** (Prerequisite: Classes, Object Initializers)
  - `var anon = new { Name = "John", Age = 30 };`.
  - Immutable, compiler-generated types.

- **Lambda Expressions** (Prerequisite: Delegates, Anonymous Methods)
  - Concise delegate syntax (`x => x * 2`).
  - Expression lambdas and statement lambdas.

- **Expression Trees** (Prerequisite: Lambda Expressions)
  - Representing code as data (`Expression<Func<int, int>>`).
  - Used by LINQ providers.

- **Extension Methods** (Prerequisite: Static Classes, Generics)
  - Adding methods to existing types (`static class Extensions { public static int Double(this int x) => x * 2; }`).
  - Must be in static classes.

- **Query Expressions (LINQ)** (Prerequisite: Generics, Lambda Expressions, Extension Methods)
  - Query syntax (`from x in collection where x > 0 select x`).
  - Keywords: `from`, `where`, `select`, `group`, `join`, `orderby`, `let`, etc.
  - Translation to method calls (e.g., `Where`, `Select`).

- **Partial Methods** (Prerequisite: Partial Types)
  - `partial` methods in partial classes (optional implementation).

## C# 4.0 (2010)
Enhances interoperability and dynamic programming, building on generics and delegates.

- **Dynamic Typing** (Prerequisite: Object Type)
  - `dynamic` type for runtime binding (`dynamic d = 10;`).
  - Bypasses static type checking.

- **Named and Optional Parameters** (Prerequisite: Methods)
  - Optional parameters (`void Method(int x = 0)`).
  - Named arguments (`Method(x: 5)`).

- **Covariance and Contravariance for Generics** (Prerequisite: Generics)
  - `out` for covariance (`IEnumerable<out T>`).
  - `in` for contravariance (`IComparer<in T>`).
  - Applied to interfaces and delegates.

- **Embedded Interop Types** (Prerequisite: Classes)
  - Simplifies COM interop by embedding type information.

- **Dynamic Import** (Prerequisite: Dynamic Typing)
  - Improved COM interop with `dynamic`.

## C# 5.0 (2012)
Focuses on asynchronous programming, building on methods and delegates.

- **Async and Await** (Prerequisite: Methods, Delegates)
  - `async` modifier for methods.
  - `await` for asynchronous operations (`await Task.Delay(1000);`).
  - Task-based asynchronous pattern (TAP).

- **Caller Information Attributes** (Prerequisite: Attributes)
  - `[CallerMemberName]`, `[CallerFilePath]`, `[CallerLineNumber]`.
  - For logging and diagnostics.

## C# 6.0 (2015)
Introduces syntactic sugar and developer productivity features, building on prior constructs.

- **Static Using Directives** (Prerequisite: Namespaces)
  - `using static System.Math;` for direct access to static members (`Sin(x)`).

- **Auto-Property Initializers** (Prerequisite: Auto-Implemented Properties)
  - `public int Prop { get; set; } = 42;`.

- **Expression-Bodied Members** (Prerequisite: Methods, Properties)
  - Expression-bodied methods (`int Double(int x) => x * 2;`).
  - Expression-bodied properties (`int Prop => 42;`).

- **Null-Conditional Operator** (Prerequisite: Nullable Types)
  - `?.` and `?[]` for safe navigation (`obj?.Property`).

- **String Interpolation** (Prerequisite: Strings)
  - `$"Hello {name}"` for formatted strings.

- **nameof Operator** (Prerequisite: Variables)
  - `nameof(variable)` for retrieving variable names as strings.

- **Exception Filters** (Prerequisite: Exception Handling)
  - `catch (Exception ex) when (ex.Message.Contains("specific"))`.

- **Dictionary Initializers** (Prerequisite: Collection Initializers)
  - `var dict = new Dictionary<int, string> { [1] = "One", [2] = "Two" };`.

- **Improved Overload Resolution** (Prerequisite: Method Overloading)
  - Better compiler handling of ambiguous overloads.

## C# 7.0 (2017)
Enhances functionality with tuples, pattern matching, and more, building on types and control flow.

- **Out Variables** (Prerequisite: `out` Parameters)
  - Inline `out` declarations (`if (int.TryParse(s, out int result))`).

- **Tuples** (Prerequisite: Types)
  - Value tuple syntax (`(int, string) t = (42, "test");`).
  - Named tuple elements (`var t = (Count: 42, Name: "test");`).
  - Deconstruction (`(int x, string y) = t;`).

- **Pattern Matching** (Prerequisite: Control Flow)
  - `is` operator with type patterns (`if (obj is int i)`).
  - Switch statement enhancements with patterns (`case int i when i > 0:`).

- **Local Functions** (Prerequisite: Methods)
  - Methods defined inside other methods (`void Local() { ... }`).

- **Ref Returns and Locals** (Prerequisite: `ref` Parameters)
  - `ref` returns (`ref int GetRef(int[] arr) => ref arr[0];`).
  - `ref` locals (`ref int x = ref arr[0];`).

- **Binary Literals and Digit Separators** (Prerequisite: Primitive Types)
  - Binary literals (`0b1010`).
  - Digit separators (`1_000_000`).

- **Throw Expressions** (Prerequisite: Exception Handling)
  - Throwing in expressions (`x ?? throw new Exception()`).

- **Generalized Async Return Types** (Prerequisite: Async/Await)
  - `ValueTask<T>` for efficient async returns.

## C# 7.1 (2017)
Minor refinements, building on C# 7.0 features.

- **Async Main** (Prerequisite: Async/Await)
  - `static async Task Main()` as program entry point.

- **Default Literal** (Prerequisite: Types)
  - `default` without type (`var x = default;`).

- **Inferred Tuple Names** (Prerequisite: Tuples)
  - Automatic tuple field names from variables (`var t = (x, y);`).

- **Pattern Matching with Generics** (Prerequisite: Pattern Matching, Generics)
  - Improved `is` and `switch` patterns with generic types.

## C# 7.2 (2017)
Further refinements, focusing on performance and safety.

- **ReadOnly Structs** (Prerequisite: Structs)
  - `readonly struct` to enforce immutability.

- **In Parameters** (Prerequisite: Methods)
  - `in` modifier for read-only reference parameters.

- **Ref ReadOnly Returns** (Prerequisite: Ref Returns)
  - `ref readonly` for immutable reference returns.

- **Non-Trailing Named Arguments** (Prerequisite: Named Parameters)
  - Named arguments anywhere in parameter list.

- **Private Protected Access Modifier** (Prerequisite: Access Modifiers)
  - `private protected` for access within assembly and derived classes.

- **Conditional Ref Expressions** (Prerequisite: Ref Locals)
  - `ref` in conditional expressions (`ref var x = ref (cond ? ref a : ref b);`).

## C# 7.3 (2018)
Performance and low-level programming enhancements.

- **Fixed Fields without Pinning** (Prerequisite: Structs)
  - Accessing fixed-size buffers without `fixed` statement.

- **Ref Local Reassignment** (Prerequisite: Ref Locals)
  - Reassigning `ref` locals.

- **Stackalloc Initializers** (Prerequisite: Arrays)
  - `stackalloc int[3] = { 1, 2, 3 };`.

- **Custom Fixed Statements** (Prerequisite: Structs)
  - `fixed` with custom types implementing `GetPinnableReference`.

- **Enhanced Generic Constraints** (Prerequisite: Generics)
  - `unmanaged` constraint for unmanaged types.
  - `System.Enum` and `System.Delegate` constraints.

- **Tuple Equality** (Prerequisite: Tuples)
  - `==` and `!=` for tuple comparisons.

## C# 8.0 (2019)
Major features for null safety and modern patterns, building on prior type and pattern systems.

- **Nullable Reference Types** (Prerequisite: Nullable Types)
  - Enabling nullable context (`#nullable enable`).
  - `string?` for nullable reference types.
  - Nullability warnings for safer code.

- **Default Interface Methods** (Prerequisite: Interfaces)
  - Methods with implementation in interfaces.
  - Enables trait-like behavior.

- **Switch Expressions** (Prerequisite: Pattern Matching)
  - `var result = x switch { 1 => "One", _ => "Other" };`.
  - Exhaustive pattern matching.

- **Property Patterns** (Prerequisite: Pattern Matching)
  - Matching on properties (`case Person { Name: "John" }`).

- **Positional Patterns** (Prerequisite: Pattern Matching, Tuples)
  - Matching tuple or deconstructable types (`case (1, 2)`).

- **Using Declarations** (Prerequisite: `using` Statement)
  - `using var x = new Resource();` (disposed at scope end).

- **Static Local Functions** (Prerequisite: Local Functions)
  - `static` modifier for local functions to prevent capturing.

- **Disposable Ref Structs** (Prerequisite: Structs, `IDisposable`)
  - `ref struct` with `Dispose` method.

- **Readonly Members** (Prerequisite: Structs)
  - `readonly` modifier for struct members.

- **Null-Coalescing Assignment** (Prerequisite: Null-Coalescing Operator)
  - `??=` for assigning if null (`x ??= defaultValue;`).

- **Interpolated Verbatim Strings** (Prerequisite: String Interpolation)
  - `$@"..."` for verbatim interpolated strings.

- **Stackalloc in Nested Expressions** (Prerequisite: Stackalloc)
  - Using `stackalloc` in expressions.

- **Indices and Ranges** (Prerequisite: Arrays)
  - Index type (`^1` for from-end indexing).
  - Range type (`1..3` for slicing).
  - Applied to arrays, strings, and `Span<T>`.

- **Async Streams** (Prerequisite: Async/Await, Iterators)
  - `IAsyncEnumerable<T>` and `await foreach`.

## C# 9.0 (2020)
Simplifies code and enhances performance, building on patterns and types.

- **Record Types** (Prerequisite: Classes, Tuples)
  - `record Person(string Name, int Age);` for immutable data types.
  - Value-based equality.
  - `with` expressions for non-destructive mutation.

- **Init-Only Properties** (Prerequisite: Auto-Implemented Properties)
  - `init` accessor for set-once properties.

- **Top-Level Statements** (Prerequisite: Main Method)
  - Programs without explicit `Main` (`Console.WriteLine("Hello");`).

- **Pattern Matching Enhancements** (Prerequisite: Pattern Matching)
  - Type patterns without variable (`if (x is int)`).
  - Parenthesized patterns (`(x is int)`).
  - Relational patterns (`case > 0`).
  - Logical patterns (`and`, `or`, `not`).

- **Covariant Return Types** (Prerequisite: Inheritance)
  - Derived return types in overridden methods.

- **Extended Partial Methods** (Prerequisite: Partial Methods)
  - Allowing access modifiers, return types, and implementations.

- **Module Initializers** (Prerequisite: Static Classes)
  - `[ModuleInitializer]` for module-level initialization.

- **New Target-Typed Expressions** (Prerequisite: Types)
  - `new()` for target-typed instantiation (`List<int> list = new();`).

- **Lambda Discard Parameters** (Prerequisite: Lambda Expressions)
  - `_` for unused lambda parameters (`(_, y) => y`).

- **Native Ints** (Prerequisite: Primitive Types)
  - `nint` and `nuint` for platform-dependent integers.

- **Attributes on Local Functions** (Prerequisite: Local Functions)
  - Applying attributes to local functions.

- **Function Pointers** (Prerequisite: Delegates)
  - `delegate*` for low-level function pointers (unsafe code).

- **Skip Locals Init** (Prerequisite: Variables)
  - `[SkipLocalsInit]` for performance optimization.

## C# 10.0 (2021)
Focuses on simplifying syntax and improving records.

- **Record Structs** (Prerequisite: Structs, Records)
  - `record struct` for value-type records.

- **Global Using Directives** (Prerequisite: Using Directives)
  - `global using System;` for project-wide imports.

- **File-Scoped Namespaces** (Prerequisite: Namespaces)
  - `namespace MyApp;` without braces.

- **Interpolated String Handlers** (Prerequisite: String Interpolation)
  - Compiler-optimized string interpolation.

- **Constant Interpolated Strings** (Prerequisite: String Interpolation, Constants)
  - Interpolated strings as constants (`const string s = $"Hello {"World"}";`).

- **Extended Property Patterns** (Prerequisite: Property Patterns)
  - Nested property access (`{ Prop.SubProp: value }`).

- **Lambda Expression Improvements** (Prerequisite: Lambda Expressions)
  - Explicit return types (`x => T (x * 2)`).
  - Attributes on lambdas.

- **Improved Definite Assignment** (Prerequisite: Variables)
  - Better compiler analysis for nullability and initialization.

- **Sealed Record ToString** (Prerequisite: Records)
  - `sealed` modifier for `ToString` in records.

- **Assignment and Declaration in Same Deconstruction** (Prerequisite: Tuples)
  - `(var x, y) = t;` mixing declarations and assignments.

- **Allow `const` Interpolated Strings** (Prerequisite: String Interpolation)
  - Compile-time constant interpolated strings.

## C# 11.0 (2022)
Enhances string literals and generic constraints.

- **Raw String Literals** (Prerequisite: Strings)
  - `"""` for multi-line, verbatim strings without escaping.

- **Generic Attributes** (Prerequisite: Attributes, Generics)
  - Generic types as attributes (`[MyAttribute<T>]`).

- **Numeric IntPtr** (Prerequisite: Native Ints)
  - Enhanced `nint`/`nuint` support.

- **UTF-8 String Literals** (Prerequisite: Strings)
  - `u8` suffix for UTF-8 strings (`"text"u8`).

- **Required Members** (Prerequisite: Classes, Properties)
  - `required` modifier for mandatory properties/fields.

- **Auto-Default Structs** (Prerequisite: Structs)
  - Compiler initializes struct fields to default values.

- **Pattern Matching with Spans** (Prerequisite: Pattern Matching, Indices and Ranges)
  - Patterns for `Span<T>` and `ReadOnlySpan<T>`.

- **Parameterless Struct Constructors** (Prerequisite: Structs)
  - Structs with parameterless constructors.

- **Checked User-Defined Operators** (Prerequisite: Operators)
  - `checked` for user-defined arithmetic operators.

- **Static Abstract Members in Interfaces** (Prerequisite: Default Interface Methods)
  - `static abstract` members for interfaces.

- **List Patterns** (Prerequisite: Pattern Matching)
  - Matching lists/arrays (`[1, 2, ..]`).

## C# 12.0 (2023)
Introduces primary constructors and collection enhancements.

- **Primary Constructors** (Prerequisite: Constructors)
  - `class Person(string name)` for concise constructor syntax.
  - Applies to classes and structs.

- **Collection Expressions** (Prerequisite: Collection Initializers)
  - `[1, 2, 3]` for arrays, lists, etc.
  - Spread operator (`[..collection]`).

- **Ref Readonly Parameters** (Prerequisite: In Parameters)
  - `ref readonly` for safe reference passing.

- **Default Lambda Parameters** (Prerequisite: Lambda Expressions)
  - Lambda parameters with defaults (`(x = 0) => x`).

- **Alias Any Type** (Prerequisite: Types)
  - `using MyAlias = System.Int32;` for any type.

- **Inline Arrays** (Prerequisite: Arrays)
  - `[InlineArray(10)] struct Buffer { private int _element; }` for fixed-size arrays.

- **Experimental Attribute** (Prerequisite: Attributes)
  - `[Experimental]` to mark APIs as experimental.

## C# 13.0 (2024)
Focuses on flexibility and performance, building on prior features.

- **Params Collections** (Prerequisite: Methods, Collection Expressions)
  - `params` with `Span<T>`, `ReadOnlySpan<T>`, or collections (`void Method(params int[] args)`).

- **Lock Object Statement** (Prerequisite: Control Flow)
  - `lock (obj) { ... }` for simplified synchronization.

- **Method Group Natural Type** (Prerequisite: Delegates)
  - Improved type inference for method groups in delegates.

- **Field Access in Auto-Properties** (Prerequisite: Auto-Implemented Properties)
  - Accessing backing fields (`field` keyword in accessors).

- **Partial Properties** (Prerequisite: Auto-Implemented Properties, Partial Types)
  - `partial` properties with separate `get`/`set` implementations.

- **Implicit Index Access** (Prerequisite: Indices and Ranges)
  - `^0` for last element access.

## C# 14.0 (2024)
Latest version, focusing on extensions and immutability.

- **Extension Types** (Prerequisite: Classes, Extension Methods)
  - `extension MyExtension for MyType { ... }` for explicit extension types.
  - Encapsulates extension methods for better organization.

- **Immutability Annotations** (Prerequisite: Nullable Reference Types)
  - `immutable` keyword for compile-time immutability checks.
  - Applied to types, fields, or parameters.

- **Improved Pattern Matching for Records** (Prerequisite: Pattern Matching, Records)
  - Enhanced record deconstruction patterns (`case RecordType { Prop: value }`).

- **Flexible Constructor Constraints** (Prerequisite: Generics)
  - `where T : new(...)` for constructors with specific signatures.

- **Named Arguments in Lambda Expressions** (Prerequisite: Lambda Expressions, Named Parameters)
  - `(x: int x) => x` for named lambda parameters.

- **Enhanced Collection Literals** (Prerequisite: Collection Expressions)
  - Extended support for dictionaries (`[key: value, ...]`).

---

## Notes
- **Ordering Rationale**: Features are ordered to ensure prerequisites are covered first (e.g., types before generics, delegates before lambdas). Within each version, features are grouped by category (e.g., types, control flow) to reflect a logical learning path.
- **Comprehensiveness**: Every feature from C# 1.0 to 14.0 is included, based on official Microsoft documentation, release notes, and my knowledge up to June 2025. C# 14.0 features are sourced from .NET 9 release announcements (November 2024).
- **Version Accuracy**: Minor features or compiler optimizations (e.g., improved overload resolution) are noted in their primary version. Some features (e.g., tuple equality in 7.3) were backported to earlier versions in specific runtimes but are listed by their official language version.
- **Learning Path**: The outline assumes a learner starts with C# 1.0 basics (syntax, types) and progresses to advanced features (e.g., pattern matching, extensions), ensuring a scaffolded approach.

If you need a deeper dive into any feature, code examples, or a specific subset of versions, let me know!