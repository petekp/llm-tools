## Note for Language Models:

When engaging in conversations related to this codebase:

- **Focus Areas:**
  - Understanding the existing architecture and implementation details.
  - Assisting with code changes, additions, and optimizations.
  - Ensuring compatibility with the current stack and adherence to best practices.
- **Communication Style:**
  - Provide clear, concise explanations.
  - Develop a comprehensive understanding of the user's goals before leaping into code.
  - Use technical language appropriate for working with experienced software engineers.
  - When suggesting code, ensure it aligns with the technologies listed.
  - Assume that libraries and modules mentioned by the user have already been installed.

---

## Strict Coding Guidelines:

When adding or modifying anything in this codebase, you MUST adhere to these guidelines:

- **General:**
  - Aim for simple, elegant, readable code; do not over-engineer or use esoteric language features.
  - Do not add JSDocs unless specifically requested.
  - Do not add comments that are obvious/self-explanatory unless requested, 
    even if you think it helps clarify the changes you've made. Assume I am capable of understanding your code.
- **CSS:**
  - If a className contains enough tailwind classes that it'd take more than a moment to decipher, use the cn utility to chunk the classes in a sensible way.
  - Always use the flex gap tailwind class instead of the "space" utility class, e.g. use "flex flex-col gap-4" instead of "space-y-4".
  - Use "size-{n}" over "w-{n} h-{n}"
  - In client components, use the cn (classnames) utility to help chunk Tailwind classes in a way that is sensible and easy to parse.
  - Prefer overflow-clip instead of overflow-hidden unless there's a specific reason.
  - 9 times out of 10 we should use container queries instead of media queries, especially when working on more atomic components. We have @tailwindcss/container-queries installed, so we should use that syntax which follows these rules:
    - Parent element has @container/{optional-id}
    - Children use the @lg:{style} syntax to apply container-query-bound styles
    - When used with the fluid-tailwind library, use "~@:~text-xl/2xl" syntax to use fluid styles with container styles together
- **Typescript:**
  - NEVER UNDER ANY CIRCUMSTANCES USE THE `any` TYPE.
  - AGAIN, DO NOT UNDER ANY CIRCUMSTANCES USE THE `any` TYPE!
  - DO NOT USE IMMEDIATELY INVOKED FUNCTION EXPRESSIONS in REACT COMPONENTS.
  - Strongly prefer an object parameter for functions over multiple parameters.
  - Define prop interfaces _inline_ rather than extracting them into a separate type or interface, unless otherwise specified, e.g. ``` function doThing({thing}: {thing: string}) {}``` instead of ```type DoThingParams = { thing: string}; function doThing({thing}: DoThingParams) {}```