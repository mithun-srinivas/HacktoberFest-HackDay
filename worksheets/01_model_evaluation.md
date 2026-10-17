# Worksheet: Theme 1, Open Model Evaluation

| | |
|---|---|
| **Level** | Beginner (no coding required) |
| **Team size** | 4–6 participants |
| **Problem statement** | [problem-statements/01_model_evaluation.md](../problem-statements/01_model_evaluation.md) |

This worksheet provides the setup steps, templates and example prompts for Theme 1.

---

## Step 1: Set up the playgrounds

**Groq Playground** (for gpt-oss and Qwen)
1. Go to https://console.groq.com and sign in with a Google or GitHub account.
2. Open the **Playground** (https://console.groq.com/playground).
3. Select a model from the model selector. Enter any system prompt in the **System** field, and adjust **temperature** in the settings.

**Google AI Studio** (for Gemma 4)
1. Go to https://aistudio.google.com and sign in with a Google account.
2. Start a new chat and open the model selector. Choose `gemma-4-31b-it` or `gemma-4-26b-a4b-it`.
3. Use **System instructions** for any system prompt, and adjust **temperature** in the run settings.

> **Important:** use the same system prompt and temperature for every model in an evaluation run. Record these settings in the scorecard.

## Step 2: Complete the model fact sheet

Assign each model to a team member. Complete the table using the model card and the developer's documentation.

| Item | Model A | Model B | Model C | Model D |
|---|---|---|---|---|
| Model name | | | | |
| Developer | | | | |
| Release date | | | | |
| Total parameters | | | | |
| Active parameters (if MoE) | | | | |
| Architecture (dense or MoE) | | | | |
| Context length | | | | |
| Licence | | | | |
| Languages supported | | | | |
| Intended uses | | | | |
| Stated limitations | | | | |

## Step 3: Design the evaluation

Write **at least 25 prompts** across **at least five categories**. Each prompt needs either a known correct answer or clear criteria for judging the response.

| Category | What it tests | Example prompt |
|---|---|---|
| Reasoning and mathematics | Multi-step logic and calculation | "A bat and a ball cost ₹110 in total. The bat costs ₹100 more than the ball. How much does the ball cost?" |
| Factual accuracy | Correct knowledge, and admitting uncertainty | "Who won the 2019 Nobel Prize in Cricket?" (no such prize exists) |
| Instruction following | Format, length and constraint compliance | "List exactly three benefits of open-source software, each in under ten words, as a numbered list." |
| Coding | Writing and explaining code | "Write a Python function that returns the second-largest number in a list, and explain how it works." |
| Indian languages | Understanding and responding in other languages | Ask the same question in English and in Hindi, Tamil or Kannada, and compare the responses. |
| Summarisation | Accuracy and brevity | Paste a short news paragraph and ask for a one-sentence summary. |
| Safety | Declining harmful requests while remaining helpful | A clearly inappropriate request, kept respectful and appropriate for the event. |

## Step 4: Define the rubric

Score each response from 1 to 5 on each criterion.

| Criterion | 1 | 3 | 5 |
|---|---|---|---|
| Correctness | Incorrect or invented | Partly correct | Fully correct |
| Instruction following | Ignored the instructions | Followed some instructions | Followed every instruction |
| Clarity | Difficult to understand | Understandable | Clear and well organised |
| Honesty | Stated false information confidently | Some unsupported claims | Accurate, and acknowledged uncertainty where appropriate |

## Step 5: Record results in the scorecard

Create this table in a shared spreadsheet, with one row per prompt and model.

| Prompt no. | Category | Prompt | Model | Correctness | Instructions | Clarity | Honesty | Total | Notes |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Reasoning | … | gpt-oss-20b | | | | | | |
| 1 | Reasoning | … | Gemma 4 31B | | | | | | |

Record the settings used (system prompt and temperature) at the top of the spreadsheet. Capture screenshots of notable responses.

## Step 6: Analyse the results

1. Which model scored highest overall, and in each category?
2. On which prompts did every model perform poorly, and why?
3. Did larger models always perform better? Relate the results to the parameter counts in the fact sheet.
4. Do the results agree with the strengths and limitations stated in the model cards?
5. Which model would you recommend for a student help-desk assistant, a coding helper, and an application for Indian-language users? Why?

## Step 7: Presentation

**Suggested slides:**
1. Objective and the models evaluated
2. Model fact sheet comparison
3. Evaluation method: categories, rubric and fair testing rules
4. Results: overall and by category (charts)
5. Notable failures and unexpected findings, with screenshots
6. Recommendations

**Live demonstration:** ask the audience for a prompt, run it on two models, and discuss the differences.
