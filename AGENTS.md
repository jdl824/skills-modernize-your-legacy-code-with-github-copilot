# AGENTS.md — Agent instructions for this repository

Purpose: Help AI coding agents quickly understand, run, and safely modify this small COBOL example.

Quick facts
- Repo language: COBOL (simple, instructional example)
- Key sources: `src/cobol/main.cob`, `src/cobol/operations.cob`, `src/cobol/data.cob`
- Docs: see [docs/README.md](docs/README.md) and [README.md](README.md)

Recommended local workflow (minimal)
1. Install GnuCOBOL (or another COBOL toolchain) if you need to compile and run locally.
2. Compile the programs together:

```
cobc -x -o account src/cobol/main.cob src/cobol/operations.cob src/cobol/data.cob
```

3. Run the app interactively:

```
./account
```

What agents should know and do
- Preserve behavior: keep the existing business rules (initial balance 1000.00; credit, debit, view; reject overdrafts).
- Run the compile step above when proposing runtime changes; prefer small, focused edits that are easy to test.
- Link to existing docs rather than copying them: use [docs/README.md](docs/README.md) for architecture and flow.
- When changing data persistence, note this repo uses an in-memory/value-based `DataProgram` (no DB). Ask before introducing external storage.
- Avoid formatting-only changes to COBOL layout unless required; COBOL can be sensitive to layout in some toolchains.

Common pitfalls
- Do not assume tests exist — this repo has no automated test suite. Validate changes by compiling and running the program.
- Be explicit when renaming program IDs or CALL names: `MainProgram`, `Operations`, and `DataProgram` are linked by name.

If unsure
- Ask the repo owner for guidance before large refactors or adding new persistent storage.

Suggested next customizations
- Add a small test harness or CI job that compiles the COBOL sources to verify changes automatically.
- Add a CONTRIBUTING.md with preferred development and PR practices for this exercise.

---
Generated to help AI agents be productive with minimal assumptions.
