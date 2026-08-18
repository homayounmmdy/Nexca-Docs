*   **Comments are a Failure:** They are a necessary evil. If code is expressive enough, comments shouldn't be needed. Code is the only source of truth; outdated comments lie and mislead.
*   **Clean Code > Comments:** Do not use comments to explain bad code. Clean the code instead.
*   **Good Comments:** 
    *   **Legal:** Copyright/license headers.
    *   **Intent:** Explains *why* a decision was made, not *how* it works.
    *   **Warnings:** Alerts about consequences (e.g., thread safety issues).
    *   **TODOs:** Acceptable reminders, but must be cleaned up regularly.
    *   **Public APIs:** Javadocs are necessary and helpful for public libraries.
*   **Bad Comments:** 
    *   **Redundant:** Repeats what the code already clearly says.
    *   **Mumbling:** Unclear and forces the reader to look elsewhere to understand.
    *   **Commented-Out Code:** Just delete it; version control (Git) remembers it.
    *   **Journal/Noise:** Logging changes or stating the obvious (e.g., `// Default constructor`).
*   **Misleading & Mandated:** Inaccurate comments cause bugs. Mandating comments (like requiring JSDoc on every variable) just creates clutter and lies.
*   **Noise & Redundancy:** Comments that restate the obvious (e.g., `// default constructor`) or act as change logs (journal comments) are useless. Use Git for history.
*   **Code over Comments:** Use well-named variables and functions to explain complex logic instead of writing a comment. Short, well-named functions don't need header comments.
*   **Commented-Out Code:** Never leave it in the file. Others will be afraid to delete it. Just delete it; version control will remember it.
*   **Formatting Clutter:** Avoid position markers (`// --- Actions ---`), closing brace comments (`} // end if`), and HTML tags in comments. If you need closing brace comments, your function is too long.
*   **Context & Relevance:** Don't include non-local system info, irrelevant historical details, or attributions ("Added by Bob"). The connection between the comment and the code must be immediately obvious.
*   **Public vs. Private:** Documentation (like JSDoc) is great for public APIs but adds unnecessary cruft to internal/private code.
