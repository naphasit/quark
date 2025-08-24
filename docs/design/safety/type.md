# Type Safety

## Table of Contents
1. [Variable Size](#variable-size)
    - [Static Size](#static-size)
    - [Dynamic Size](#dynamic-size)
    - [Assignment Rules](#assignment-rules)
2. [Data Type](#data-type)
    - [Data Types](#data-types)
    - [Type of Declare Statement](#type-of-declare-statement)
    - [Type naming](#type-naming)
3. [Built-in Data Types](#built-in-data-types)
4. [Type Conversion](#type-conversion)

# Concept
Quark enforces **static typing** and has specific rules for type assignments, particularly regarding **variable sizes** and the **data types**.
1. ## Variable Size
    - **Every variable** in Quark **must specify its size**. Variables can be either static size or dynamic size, with different assignment rules.
    - ### Static Size
       - The size of the variable is **fixed at compile time**.
       - Store data on the **stack**.
    - ### Dynamic Size
       - The size of the variable **can change at runtime**.
       - Store data on the **heap**.
    - ### Assignment Rules
        - **Static** → **Static** (same size & type) => **Allowed**.
        - **Static** → **Static** (different size) => **Not Allowed**.
        - **Static** → **Dynamic** => **Allowed**.
        - **Dynamic** → **Static** => **Not Allowed**.
2. ## Data Types
    - ## Type Declaration
       - **Every variable must specify its type**.
    - ## Type of Declare Statement 
       - Alias: **alternative name** for an **existing type** (just a synonym).
       - Enum: a set of **named constant values**.
       - Struct: **structured** type that encapsulates **related data**.
    - ## Type naming
       - Must use **PascalCase**.
       - Applies to both **types names** and **generic type parameters**.
       - Examples: `MyString`, `Foods`, `SpiderType`, `Result<T>`.
3. ## Built-in Data Types
    - `Bool`: Boolean(`true` or `false`)
    - `Char`: Unicode Character (**Single Character**)
    - `U8`: 8-Bits of Unsigned Integer
    - `U16`: 16-Bits of Unsigned Integer
    - `U32`: 32-Bits of Unsigned Integer
    - `U64`: 64-Bits of Unsigned Integer
    - `U128`: 128-Bits of Unsigned Integer
    - `I8`: 8-Bits of Signed Integer
    - `I16`: 16-Bits of Signed Integer
    - `I32`: 32-Bits of Signed Integer
    - `I64`: 64-Bits of Signed Integer
    - `I128`: 128-Bits of Signed Integer
    - `Array<T>`: Array of `T`.
    - `String`: Alias for `Array<Char>` (**dynamic**).
    - `Maybe<T>`: Nullable type (`Valid<T>` or `Invalid`).
    - `Result<T, E>`: Error-handling type (`Success<T>` or `Failure<E>`).
4. ## Type Conversion
    - Widening conversion (**safe**) => **Allowed**
       - Example: `U32` → `U64`
    - Narrowing conversion (**unsafe**) => **Not Allowed**
       - Example: `U64` → `U32`