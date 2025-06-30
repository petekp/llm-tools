# 🧹 Prompt: Mid-Feature Cleanup & Refactor Audit

You are my engineering partner. I’ve made substantial progress on a feature, and now it’s time to pause and **take stock of what’s been built so far**.

Your job is to help me **identify areas that could use cleanup, simplification, or refactoring** so I can move forward on a solid foundation without accruing avoidable tech debt.

---

## 1. Code Smell & Clutter Check

- Are there any sections of code that feel overly complex, repetitive, or hard to follow?
- Are there inline comments, TODOs, or WIP logic that should be revisited or resolved?
- Are we relying on "just get it working" hacks that could bite us later?

---

## 2. Redundancy & Abstraction

- Are there patterns or logic repeated across files/components that should be pulled into helpers or custom hooks?
- Is anything over-abstracted or prematurely generalized?
- Are there clear seams for small refactors that would simplify the code without over-engineering?
- When dealing with zod schemas, ensure we're utilizing utilities like @unwrapZodType.ts, @getChildSchemaMetadata.ts, @getElementSchemaAndMetadata.ts, @processDiscriminatedUnionOptions.ts, @getDiscriminatorValue.ts rather than doing this work from scratch.

---

## 3. Risk & Fragility Zones

- Are there any parts of the code that feel brittle or too tightly coupled?
- Are assumptions (about types, data shapes, loading states, etc.) being made that should be revisited?

---

## 4. DX & Maintainability

- Is the naming consistent and clear across files and functions?
- Would another engineer understand how to pick up where this leaves off?
- Are file boundaries logical and easy to navigate?

---

## 5. Engineering Protocol Alignment

You must **carefully assess all code through the lens of our team’s engineering protocols**, which will be provided separately.

- Identify any places where the current code **deviates from or only partially fulfills** those protocols.
- Clearly note where things are solid, and where they can be improved to better meet our standards.
- If a judgment call is required, **briefly explain the tradeoff** and suggest the lowest-effort fix that meaningfully improves adherence.

---

## Format

- Use bullet points grouped by concern type (e.g., "Naming", "Brittle Logic", "Overuse of Optional Chaining")
- Refer to files and line numbers when possible
- Avoid suggesting tests or new features — this is purely about **cleaning up and tightening what's already there**

---

## Constraints

- **Do not suggest adding tests or changing external behavior.**
- **Do not propose large architectural rewrites.**
- Stay focused on small-to-medium refinements that improve clarity, structure, and confidence without derailing velocity.