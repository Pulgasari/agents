# code

## language & environment
- **language:** plain javascript. no typescript, except central type declarations (`index.d.ts`) for packages.
- **target:** browser-first and esm-native. keep cross-runtime/bundler compatibility (node, deno, bun, vite), but native browser execution has priority.

## priorities
- **performance and readability** above all else.
- **performance auditing:** explicitly flag critical bottlenecks and anti-patterns and explain the underlying technical cause.

## structure
- **modularization:** split package logic into separate files where sensible, but do not over-modularize (no file for every tiny utility).
- **ordering:** sort alphabetically and group logically wherever applicable (imports, exports, options, properties, ...).

## formatting
- **indentation:** 2 spaces.
- **parentheses:** space between identifier and parentheses, none inside. applies to function declarations and methods:
  ```js
  function name (arg, arg2) {}
  method (arg) {}
  ```
- **compact but readable:** one-liners are fine wherever they fit. short conditionals belong on one line, not three:
  ```js
  if (condition) doSomething();
  ```
- **alignment:** align similar or identical consecutive lines:
  ```js
  const abc   = null;
  const heino = new Date;
  ```
- **`new` without arguments:** omit the parentheses (`new Date`, not `new Date()`).

## naming
- **case:** `camelCase`.
- **no useless abbreviations:** `value`, not `val` or `v`. common, natural abbreviations are fine (`decl` for `declaration`), as is shortening names that are really long.

### whitelist
- `declaration` -> `decl`
- `declarations` -> `decls`
- `definition` -> `def`
- `definitions` -> `defs`

## comments
- **as few as possible:** do not litter the code with comments. nothing that explains obvious or trivial code.
- **no doc comments** (jsdoc etc.) in code. documentation is done separately afterwards (`index.d.ts`, docs files).
- **style:** english, entirely lowercase (uppercase only for explicit emphasis), technical, to the point, no emojis.
