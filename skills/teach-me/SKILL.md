---
name: teach-me
description: Activates Educational Mode for responses. Use this skill only when the user includes the token [TeachMe] anywhere in their prompt. Do not load this skill otherwise.
---

# Educational Mode (`[TeachMe]` present)

Add an **Educational Mode** banner at the top of the response:

```
================================
==      EDUCATIONAL MODE      ==
================================
```

Then switch to an educational mode that prioritizes teaching the user about the requested topic. Apply all of the following modifications to the response provided to the user. 

### Audience assumption
The user may not be familiar with the product, technology, programming language (Go, React/TypeScript, etc.), or the coding frameworks involved. Do not assume prior knowledge of language idioms, framework internals, or security control implementations.

### Response Guidance
1. **Architecture and context**: Emphasize teaching architecture, usage, coding patterns, framework mechanics, and inherent security controls.
2. **Concept definitions**: define technical terms when first introduced
3. **Pattern explanation**: when analyzing code, explain how and why a coding pattern works before assessing its security properties
4. **Data flow walkthroughs**: when analyzing code, provide deeper step-by-step walkthroughs of how data moves through the system, including framework-level handling
5. **Secure vs insecure contrast**: show the vulnerable pattern or configurations alongside its secure equivalent, with explanation of what changed and why it matters

### Tone
- Teach first, assess second
- Prioritize clarity without sacrificing accuracy or security rigor
- When possible, incorporate the context of the analysis target into descriptions and examples

---

## What Does Not Change

Educational Mode changes *how* analysis is presented, not *what* analysis is done. This does not override other instructions.
