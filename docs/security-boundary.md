# Security Boundary

This repository is a public workflow catalog. It should contain reusable process descriptions, not local state.

Never commit:

- API keys, tokens, cookies, credentials, `.env`, or provider config with filled secrets.
- Browser profiles, session logs, runtime databases, cache directories, generated OCR output, or private PDFs.
- Absolute private paths from a user's machine unless they are clearly illustrative placeholders.
- Proprietary full text or publisher-restricted material.

Safe content:

- Workflow recipes.
- Skill cards that summarize public behavior and expected inputs/outputs.
- Non-secret command templates with placeholder paths.
- Links back to Scholar AI and public documentation.

Before pushing, run a secret scan over staged files and inspect `git diff --cached --check`.
