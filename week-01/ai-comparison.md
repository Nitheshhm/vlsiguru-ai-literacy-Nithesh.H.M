# Week 01 AI Assistant Comparison
## Common question
In Python, what does list.sort() return? Does it modify the original list? Also explain the difference between list.sort() and sorted().

## Tool 1
**Name:** ChatGPT
**Answer summary:** ChatGPT explained that `list.sort()` returns `None` and modifies the original list in place. It also explained that `sorted()` returns a new sorted list while leaving the original list unchanged.
**Strengths:** Clear and concise explanation with a direct example.
**Weaknesses:** Less detailed than Claude's response.

## Tool 2
**Name:** Claude
**Answer summary:** Claude explained that `list.sort()` returns `None` and modifies the original list in place. It explained that `sorted()` returns a new sorted list and does not modify the original list. It also provided examples and additional information about iterables and sorting options.

**Strengths:** More detailed explanation with multiple examples and a comparison table.
**Weaknesses:** More detailed than necessary for the simple question.

## Verification source
**Python Documentation — Sorting Techniques**

https://docs.python.org/3.13/howto/sorting.html
The Python documentation confirms that `list.sort()` sorts a list in place and returns `None`, while `sorted()` returns a new sorted list.

## Final comparison
- **Accuracy:** Both assistants gave answers consistent with the Python documentation.
- **Traceability:** The answers were checked against the official Python documentation.
- **Explanation quality:** ChatGPT gave a concise explanation, while Claude provided more detail and examples.
- **Ease of verification:** Both answers were easy to verify because the official Python documentation clearly states the behavior.
- **Which claims required correction or qualification?** No main claim required correction. Both assistants were correct for this question.

## Lesson
I learned that different AI assistants can give correct answers while differing in detail, structure, and explanation style. A more detailed answer is not automatically more accurate. I should compare important claims with a reliable reference instead of judging an answer only by how confident or detailed it sounds.
