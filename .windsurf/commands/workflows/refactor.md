# refactor

1. Review only the files changed for the current task and their directly related modules.
2. Refactor only if it materially improves navigability for future agents.
3. Prefer small, safe refactors:
   - Split large files (target under 500 LOC)
   - Organize into clear folder hierarchies
   - Tighten module boundaries; remove dead code
4. Keep behavior identical.
5. Ensure top-of-file docs remain accurate.
