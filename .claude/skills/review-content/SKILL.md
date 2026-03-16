---
name: review-content
description: Review slide content for logical consistency, clarity, and presentation quality. Use to improve slides before a meeting.
disable-model-invocation: true
allowed-tools: Read, Glob, Grep
---

Review slide content for quality and logical consistency.

## Arguments

`$ARGUMENTS` should be one of:
- A path to a specific `slides.md` file
- A date folder like `2026/03-18`
- Empty — reviews the most recent slide deck

## Review Criteria

1. **Logical flow**: Do slides follow a coherent narrative? Flag contradictions between slides.
2. **Consistency**: Are claims in results slides supported by the discussion? Do conclusions match the evidence presented?
3. **Clarity**: Is each slide's message clear? Flag slides that try to convey too many points.
4. **Emphasis**: Is `***bold italic***` (blue highlight) used effectively for key findings?
5. **Completeness**: Are there gaps in the story? (e.g., methods shown but no results, results without discussion)
6. **Conciseness**: Flag slides with too much text that could overflow.

## Output

For each issue found:
- Slide number and title
- The problem
- A specific suggestion for improvement

End with an overall assessment and top 3 priority improvements.
