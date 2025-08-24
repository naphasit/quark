# Type Safety

# Concept
Quark enforces **static typing** and has specific rules for type assignments, particularly regarding **variable sizes** and the **data types**.
1. ## Variable Size
    - Every variable in Quark must **specify its size**. Variables can be either static size or dynamic size, with different assignment rules.
    - ### Static Size
       - The size of the variable is **fixed at compile time**.
       - Store data on the **stack**.
    - ### Dynamic Size
       - The size of the variable **can change at runtime**.
       - Store data on the **heap**.
    - ### Assignment Rules
        - Static → Static (same size & type) => Allowed.
        - Static → Static (different size) => Not Allowed.
        - Static → Dynamic => Allowed.
        - Dynamic → Static => Not Allowed.
2. ## Data Types
    - ## Type Declaration
       - Every variable must specify its type.
    - ## Type of Declare Statement 
       - Alias: **alternative name** for an **existing type** (just a synonym).
       - Enum: a set of **named constant values**.
       - Struct: **structured** type that encapsulates **related data**.
    - ## Type naming
       - Must use **PascalCase**.
       - Applies to both **types names** and **generic type parameters**.
       - Examples: `MyString`, `Foods`, `SpiderType`, `Result<T>`.