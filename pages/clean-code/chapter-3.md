*   **Small:** Functions should be tiny. Ideally 2–4 lines, rarely over 20.
*   **Do One Thing:** A function should do exactly one thing, do it well, and do it only. If you can extract another meaningful function from it, it is doing too much.
*   **One Level of Abstraction:** Never mix high-level concepts (e.g., `renderPage()`) with low-level details (e.g., string concatenation) in the same function.
*   **The Stepdown Rule:** Code should read top-down like a narrative. Each function should call functions that are exactly one level of abstraction below it.
*   **Switch Statements:** They inherently do multiple things and violate SRP/OCP. Bury them in low-level factories and use polymorphism instead.
*   **Descriptive Names:** Long, descriptive names are better than short, cryptic names or comments. Be consistent (e.g., `includeSetupPages`, `includeTeardownPages`).
*   **Function Arguments:** 0 is ideal, 1 is good, 2 is acceptable, 3 should be avoided, and >3 is unacceptable. Arguments increase cognitive load and make testing exponentially harder.
*   **Argument Rules:** 0 arguments is ideal, 1 is good, 2 is acceptable, and 3+ should be avoided. Wrap multiple arguments into a single object (e.g., `Point` instead of `x, y`). 
*   **No Flag Arguments:** Passing a boolean (e.g., `render(true)`) is terrible practice. It loudly proclaims the function does more than one thing. Split it into two functions (e.g., `renderForSuite()`, `renderForTest()`).
*   **No Side Effects:** A function must not secretly change state (e.g., a `checkPassword` function should not secretly call `Session.initialize()`). This creates dangerous temporal coupling.
*   **Command Query Separation:** A function should either *do* something (command) or *answer* something (query), but never both. 
*   **Prefer Exceptions to Error Codes:** Returning error codes forces deeply nested `if` statements. Use exceptions to separate error handling from the "happy path."
*   **Extract Try/Catch Blocks:** `try/catch` blocks are ugly. Extract the `try` body and `catch` body into their own separate functions so the main function's intent remains clear.
*   **Error Handling Is One Thing:** If a function contains a `try` block, it should be the very first word, and nothing should follow the `catch`/`finally` blocks.
*   **DRY (Don't Repeat Yourself):** Duplication bloats code and multiplies the chance of errors. Extract repeated logic into single, well-named functions.
*   **The Refactoring Process:** Write a clumsy, long first draft. Then continuously massage, split, rename, and shrink it while keeping unit tests passing.
