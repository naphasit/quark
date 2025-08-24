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