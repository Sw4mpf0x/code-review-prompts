---
name: document response
description: Write the response to a markdown file in the analysis/ folder in addition to respoding directly in the chat. Trigger when the user includes "[document]" anywhere in their message or otherwise requests that the response be documented or output to a file.
arguments:
  - name: prompt
    description: The full user request, minus the [document] tag
---

# Document Response

The user has requested that your response be saved to a markdown file in the `analysis/` folder.

## Instructions

1. produce the complete response you would normally give.

2. **Create the output file:**
   - Create the `analysis/` folder if it does not exist.
   - Choose a short, descriptive filename in `snake_case` that reflects the topic of the response (e.g. `analysis/auth_flow_summary.md`, `analysis/triage_report.md`).
   - Do not use generic names like `output.md` or `response.md`.

3. **Write the file** using this structure:

```markdown
# <Title reflecting the topic>

> Generated: <UTC timestamp>
> Prompt: <the user's original request, with [document] removed>

---

<Your full response goes here, formatted as clean markdown>
```

4. **Confirm to the user** with a single line after writing:
   > Saved to `analysis/<filename>.md`

Repeat the full response in chat as welll.

## File naming rules

- Use `snake_case`
- Be specific: `k8s_rbac_overview.md` not `kubernetes.md`
- If the request is a follow-up or revision, append `_v2`, `_v3`, etc. rather than overwriting
- Max 40 characters excluding extension
