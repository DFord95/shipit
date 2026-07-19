# Insecure examples (for Lab 4, Step 6)

These are **deliberately vulnerable** snippets used to prove the security gate blocks a
bad change. They are stored as `.cs.txt` so they are **not** compiled into the app or
scanned on `main` — you copy one into real code inside a pull request to watch CodeQL
flag it, then replace it with the fixed version.

- `CommandInjectionExample.cs.txt` — a `/trace/{host}` endpoint that passes user input
  straight into a shell (CodeQL: `cs/command-line-injection`), plus a fixed version that
  takes no shell and validates input.

Do not ship any of this in a real service.
