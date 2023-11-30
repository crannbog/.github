# Code Manifest (WIP)

This manifest collects principles of how we want to write code / software.

## Code conventions (including JS specific conventions)

- Naming variables, functions, ... 
  - You don't need to document functionality if your code is self-explaining
  - use descriptive names for functions and variables, even if they get long. Variables: Describe what it *is*, Functions: Describe what it *does* 
  - functions should do one job, not multiple, with a func name describing the job
  - Events:
    - Listeners: `onXXX`, like `onClick`
    - Handlers (to bind on a listener): `handleXXX`, like `onClick={handleClick}`


- Consistent naming:
  - Classes, components (+ filenames), singletons: `PascalCase`
  - Functions, variables, classNames, other filenames: `camelCase`
  - unused properties/members/variables: `_camelCase` (camelCase with leading underscore)
  - private properties/members/variables: `__camelCase` (camelCase with double leading underscore)

- Be aware of concepts like **pure functions, immutability, ...** and use them per default
  - Prefer `const` variables
  - Prefer array functions over external loops

- Avoid switch/case, prefer if/return

- If you have to copy/paste blocks of code you might doing something wrong
  - consider creating reusable + shared code

## Handling Environments

- Configure environments by scripts
  - try not to do a single configuration you want to keep by hand - always create scripts to document configuration and make a setup recreateable
