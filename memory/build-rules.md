# Build Rules (local implementation and portable briefs)

This is the single source of truth for standing implementation rules. Build & Protect reads and applies them while building in this workspace. A brief exported to another session or tool must carry these rules because that destination may not have this repository.

**How the agents use this file:** local implementation records link to and apply this file. Every portable implementation brief, including one for Claude Code or another agent, must embed this full file verbatim at the end under "STANDING BUILD RULES (implementation must follow)." Do not paraphrase, summarize, or trim. Always use the current version.

**How you grow it:** add a new rule to the list below. It will automatically appear in every brief produced after that. Keep each rule short, concrete, and testable.

---

## RULES

1. **No dashes.** Never use em dashes or en dashes anywhere: not in UI copy, code comments, documentation, commit messages, variable names, or any generated text. Use a period, comma, colon, or parentheses instead. (The characters to avoid are the long dash and the medium dash; ordinary hyphens in compound words and code are fine.)

<!-- Add new build rules below this line, numbered. They will be carried into every future brief. -->
