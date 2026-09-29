# AI-Use Log

**Tool/Date:** WorkBuddy AI [Today's Date]
**Purpose:** Design a safe, repeatable annotation prompt for possible anxiety language in public posts for first-year HKBU students.

**Prompt Used:**
> "We are annotating a Kaggle mental health public repository about possible anxiety language for first-year HKBU students in Hong Kong. Our purpose is to understand what a text label can and cannot mean. Give us a table with post ID, label, evidence span, and confidence. Separate text evidence from inference. State uncertainty and allow ABSTAIN. Do not infer diagnosis, identity, age, or risk. Do not invent statistics or provide treatment advice. Before answering, ask us three clarifying questions about audience, purpose and risk."

**Useful Output:**
- WorkBuddy proposed label definitions and edge cases.
- It generated an HTML artifact (`annotation_framework.html`) with a CSV template.
- **Strongest example:** EX-007 ("Exam in 2 hours. I'm going to die."). It correctly labeled this as `ABSTAIN` because the text is ambiguous (hyperbole vs. distress) and lacks context.

**Human Decisions & Rejections:**
- I set the risk level to "Strict" (prioritizing abstaining, avoiding re-identification, preventing false certainty).
- I rejected any diagnosis language or forced yes/no labels.
- I required WorkBuddy to ask clarifying questions before generating the table, which ensured the output fit the specific audience and purpose of the course.

**Verification:**
- The output was checked against the C.L.E.A.R. framework. It correctly abstained rather than making an unsupported inference about the writer's mental state.
