*   **Naming Rules:**
    1. **Reveal Intent:** Names must explain *why* it exists, *what* it does, and *how* it’s used. If it needs a comment, the name failed.
    2. **Avoid Disinformation:** Don’t use misleading terms (e.g., `accountList` if it’s not an actual List). Avoid visually confusing characters like lowercase `l` and uppercase `O`.
    3. **Make Meaningful Distinctions:** Don’t just add numbers or noise words (`data1`, `data2`) to satisfy the compiler. Different names must mean different things.
*   **Pronounceable & Searchable:** Use real, pronounceable words. Avoid number series (`a1`, `a2`) and redundant noise words (`Info`, `Data`, `Variable`).
*   **No Encodings:** Drop Hungarian notation (`strName`) and member prefixes (`m_`). Modern IDEs and languages handle types. Do not prefix interfaces with `I`; encode the implementation instead if necessary.
*   **Avoid Mental Mapping:** Avoid single-letter names (except `i`, `j`, `k` for small loop scopes). Readers shouldn't have to mentally decode abbreviations. Clarity is king.
*   **Naming Conventions:** Classes should be nouns (`Customer`). Methods should be verbs (`deletePage`). Use `get`, `set`, `is` for accessors/predicates. Use static factory methods for overloaded constructors.
*   **No Cuteness or Puns:** Avoid jokes or slang (`whack()` instead of `kill()`). Pick *one* word per concept (don't mix `get`, `fetch`, and `retrieve`). Don't reuse words for different actions (e.g., use `insert` for collections, reserve `add` for math).
*   **Add Meaningful Context:** Group related variables into well-named classes (e.g., `Address`) rather than using awkward prefixes. 
*   **No Gratuitous Context:** Avoid prefixing every class with an app acronym (e.g., `GSDAccountAddress`). It creates redundant noise and ruins IDE auto-complete.
