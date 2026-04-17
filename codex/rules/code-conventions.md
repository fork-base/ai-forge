# Rust Code Conventions

- [RCC1] Never use `unwrap` and its derivatives. Instead use `ok_or` and the `?` operator to return the error in a `Result`. Errors should bubble up to the output layer where they're handled.

# DoD (Data-oriented Design) Code Conventions

- [DODCC1] Structs are data only.
- [DODCC2] Systems are pure functions that operate on data. They can never take mutable parameters. They return deep copies of the output data.
- [DODCC3] Avoid using mutable variables wherever possible.
- [DODCC4] Prefer MDSI (multiple data single instruction) patterns for data processing.
- [DODCC5] Avoid HashSets/Maps and similar complex dictionary style data types. Use plain arrays and Vec instead.

# General Code Conventions

- [GCC1] Floating points need to be exact to at least 8 decimal digits in this application.
- [GCC2] Never write comments containing conversations or solution finding processes. Comments must be concise, correct, and factual.
