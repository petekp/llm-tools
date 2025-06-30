# Paired-Principal Engineer Ideation Exercise

When presented with a non-trivial engineering task (feature design, refactor, bug-hunt, algorithm choice, etc.) **and _before_ writing or editing code**, the AI should perform the following exercise:

1. **Switch perspectives** between two seasoned principal software engineers (`Engineer A` and `Engineer B`).  
   • These are not characters in a story but active participants in a technical design session.  
   • They have no preconceived solution and must reason from first principles.
2. **Iterative Back-and-Forth**  
   • Engineer A proposes an idea or approach.  
   • Engineer B critiques, refines, or offers an alternative, citing edge-cases, performance considerations, DX, scalability, readability, etc.  
   • Continue for at least **3 full exchanges** (A→B→A→B→A→B) or until a clear, elegant approach emerges.  
   • It's acceptable (and encouraged) for engineers to revise their own earlier stance when confronted with better reasoning.
3. **Avoid contrived dialogue.** Keep the conversation concise, technical, and focused—no storytelling fluff.  Aim for authenticity: real engineers discovering a solution together.
4. **Conclude** with a **Joint Decision** section summarizing the agreed-upon approach (or noting remaining trade-offs if no single winner exists).  This summary should guide subsequent code changes.

### Output format
```
Engineer A: <thought>
Engineer B: <response>
Engineer A: <refinement>
Engineer B: <response>
Engineer A: <final thought>
Engineer B: <final response>
[+ additional back and forth depending on the complexity of the problem being tackled]

Joint Decision:
- <bullet 1>
- <bullet 2>
```

This exercise should be executed **only once per task** (unless the task scope changes significantly) and placed **before any code edits** or tool calls so that the reasoning directly informs implementation decisions.
