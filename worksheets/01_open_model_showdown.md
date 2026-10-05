# Worksheet: Problem 1, Open Model Showdown

| | |
|---|---|
| **Level** | Foundation (no coding required) |
| **Team size** | 2–4 participants |
| **Problem statement** | [problem-statements/01_open_model_showdown.md](../problem-statements/01_open_model_showdown.md) |

This worksheet guides the team through a structured evaluation of three open AI models. Evaluation is the process AI research teams use to measure and compare model quality.

**Requirements:** a laptop with a web browser, a shared Google Sheet, and (optionally) a free Hugging Face account, which saves your conversation history.

---

## Step 1: Explore the tools

- **HuggingChat** (https://huggingface.co/chat): free access to open-weight models. Use the model selector to switch between models such as Llama, Qwen, Mistral, DeepSeek and Gemma. The available models change over time.
- **LMArena** (https://lmarena.ai): select **Side by Side** to send one prompt to two chosen models and compare their responses. The **Battle** mode hides model names until you vote, which makes results harder to record.
- **Groq Playground** (optional; free account required) (https://console.groq.com/playground): fast responses, with an adjustable **temperature** setting.

**Eligibility:** score only **open-weight** models, meaning models whose weights are publicly downloadable (for example Llama, Qwen, Mistral, Gemma, DeepSeek, gpt-oss and OLMo). If unsure, search for the model on huggingface.co. If it can be downloaded there, it is open-weight.

## Step 2: Select a theme

| Theme | Example prompt |
|---|---|
| Explaining concepts simply | "Explain how vaccines work to a 10-year-old." |
| Logic puzzles | "I have keys but no locks, space but no room. What am I?" |
| Arithmetic reasoning | "A bat and a ball cost ₹110 in total. The bat costs ₹100 more than the ball. How much does the ball cost?" |
| Indian languages | Ask questions in Hindi, Tamil, Kannada or another language and assess the quality of the responses. |
| Creative writing | "Write a four-line poem about Monday mornings in a college hostel." |
| Factual accuracy | Ask about something that does not exist (for example, "Who won the 2019 Nobel Prize in Cricket?") and see whether the model admits it does not know. |
| Code explanation | "Explain what this code does: `for i in range(3): print(i*i)`" |

## Step 3: Write test prompts and a rubric

Effective test prompts are **specific**, **varied in difficulty**, and **assessable**: they have either a correct answer or clear criteria for judging quality.

Select **three criteria** and score each from **1 to 5**:

| Criterion | Score of 1 | Score of 5 |
|---|---|---|
| Correctness | Incorrect or invented | Fully correct |
| Clarity | Difficult to understand | Easily understood by the intended audience |
| Instruction following | Ignored the requested length or format | Did exactly what was asked |
| Creativity | Generic | Original and engaging |
| Honesty | Stated false information with confidence | Acknowledged uncertainty where appropriate |

**Fair testing rules:**
- Use the identical prompt for every model.
- Start a new conversation for each prompt so that earlier messages do not influence the response.
- Where possible, have two team members score each response independently and average the scores.

## Step 4: Run the tests

Create the following table in Google Sheets:

| No. | Prompt | Model A | Model B | Model C | Notes |
|---|---|---|---|---|---|
| | | Correctness / Clarity / Instructions | Correctness / Clarity / Instructions | Correctness / Clarity / Instructions | |
| 1 | … | 5 / 4 / 5 | 3 / 3 / 4 | … | Model B gave ₹10 (incorrect) |
| … | | | | | |
| **Total** | | | | | |

Capture **screenshots** of the strongest response, the weakest response, and any notable or unexpected behaviour.

**Suggested roles:** one member enters the prompts, one records the scores, one captures screenshots, and all members score.

## Step 5: Analyse the results

Discuss and record answers to the following:

1. Which model scored highest overall? Did the result differ by criterion?
2. On which prompts did all models perform poorly?
3. Did larger models always perform better? (Model names often show size; for example, "8B" means 8 billion parameters.)
4. What was the most unexpected finding?
5. What recommendation would you give: "For task X, use model Y, because…"?

## Step 6: Presentation

**Slides (no more than five):**
1. Research question and theme
2. Method: the three models, the rubric, and the fair testing rules
3. Results: a bar chart of total scores (Google Sheets → Insert → Chart)
4. Notable failures and unexpected findings, with screenshots
5. Recommendation

**Live comparison:** ask the audience to suggest a prompt, run it on two models in LMArena side-by-side mode, and ask the audience to vote for the better response.

---

## Optional extensions
- **Temperature comparison:** in the Groq Playground, run the same prompt at temperature 0 and 1.5 and compare the results.
- **Model size comparison:** compare a smaller and a larger model from the same family (for example, Llama 8B and Llama 70B).
- **Safety comparison:** assess which model best declines a clearly inappropriate request while staying helpful. Keep all test content appropriate.
- **System prompt comparison:** in the Groq Playground, give each model the same system prompt and compare how consistently each follows it.

## Deliverables checklist
- [ ] Completed scorecard: 10 prompts × 3 models × rubric scores
- [ ] Results chart and overall conclusion
- [ ] Notable failures and an unexpected finding, with screenshots
- [ ] Live audience comparison
