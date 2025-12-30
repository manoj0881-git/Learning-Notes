<!-- Copilot instructions for Learning-Notes repository -->
# Copilot guidance — Learning-Notes

Purpose
- Help maintain and edit the Learning-Notes markdown collection (system-design notes, short how-tos, prototypes).

Big picture (what this repo is)
- This repository is a collection of learning notes and design assignments (markdown-first). Primary content lives as top-level markdown files and topic folders such as [OpenObserve](OpenObserve) and [System Design Learning](System%20Design%20Learning).
- Typical items: design walkthroughs (example: [online-offline-indicator.md](online-offline-indicator.md#L1)), short definitions ([dictionary-word.md](dictionary-word.md#L1)), and topic folders containing multiple notes.

What to focus on
- Edit and improve markdown content: clarity, correct headings, examples, diagrams, and TOC.
- Preserve existing structural markers: do NOT remove the repository's Table-of-Contents markers (<!--ts--> and <!--te--> blocks) or other HTML comment markers used for local TOC generation.
- Keep external image links as-is unless provided replacement assets. If adding images, prefer relative paths inside the repo or ask before adding large media.

Project-specific patterns and examples
- TOC blocks: maintain the <!--ts--> / <!--te--> blocks found at the top of many files (see [online-offline-indicator.md](online-offline-indicator.md#L1)).
- Section layout: files use clear top-level sections (Problem Statement, Requirements, Output, Outcome). When editing, follow those existing headings rather than introducing new top-level structures.
- Prototypes and tech suggestions are examples (NodeJS/SocketIO in the Online/Offline doc) — keep recommendations descriptive rather than prescriptive.

Developer workflows
- There are no build, test, or CI scripts detected in this repo; changes are content-only. For any code prototypes referenced, expect them to live in separate repos.
- When making content changes: make small, focused PRs that describe the file(s) changed and the intent (e.g., "Improve examples in System Design: Online/Offline indicator").

When to ask the maintainer
- If unsure where a new note belongs (top-level vs. System Design folder), ask before moving files.
- If adding executable code or runnable prototypes, confirm whether a dedicated sub-repo or a /prototype folder is preferred.

Do not do
- Do not convert content into executables, change repo structure without approval, or remove TOC markers and existing diagram links.

Examples (actionable)
- Edit an existing note: update the section under "Problem Statement" in [online-offline-indicator.md](online-offline-indicator.md#L1), keep the TOC markers, and add a short bullet under "You'll learn".
- Add a new design doc: create a single markdown file in the appropriate folder (System%20Design%20Learning for system design topics) with the same section pattern used across the repo.

If you need more context
- Ask for clarification mentioning the target filename and the intended change, or provide a draft in a PR for quick feedback.

End of instructions.
