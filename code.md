# Code Structure & File Organization

- **Core Focus:** Prioritize performance and readability above all else.
- **Performance Auditing:** Explicitly flag and explain any identified critical performance bottlenecks or anti-patterns, detailing the underlying technical causes.

- **Modularization:** Split package logic into separate files where sensible, but avoid over-modularizing (do not create a file for every tiny utility).
- **ordering:** sort items alphabetically and group them logically whenever applicable (e.g., imports, exports, options, properties).

- **Indentation:** 2 spaces (tabsize: 2).
- **function declarations:** include a space before and after parentheses, but none inside:
  ```js
  function name () {}
  ```

- **Naming Conventions:**
  - **Case:** Prefer `camelCase`.
  - **Descriptive Names:** Do not uselessly abbreviate variables (e.g., use `value` instead of `val` or `v`). Standard/common abbreviations are allowed when natural (e.g., `decl` for `declaration`).
- **Comments:**
  - 

## comments
- do not put unnessesary comments explaining obvious/trivial stuff into the files
- all code comments must be written in English.
- write comments entirely in lowercase, reserving uppercase solely for explicit emphasis.

## Tech Stack & Language
- **Language:** Plain JavaScript. Do **not** use TypeScript, with the sole exception of `index.d.ts` declaration files for packages.
- **Target Environment:** Browser-first and ESM-native. Maintain cross-runtime/bundler compatibility (Node.js, Deno, Bun, Vite) while prioritizing native browser execution.
