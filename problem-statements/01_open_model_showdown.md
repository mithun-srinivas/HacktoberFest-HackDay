# Problem Statement 1: Open Model Showdown

| | |
|---|---|
| **Level** | Foundation (no coding required) |
| **Team size** | 2–4 participants |
| **Duration** | Approximately 3 hours |
| **Resources** | [Detailed worksheet](../worksheets/01_open_model_showdown.md) |

---

## 1. Background

Many AI chatbots today are built on **open models**: AI models that anyone may download and use free of charge. Examples include Llama (Meta), Qwen (Alibaba), Mistral, and Gemma (Google).

These models are not equally good at every task. One model may perform well at creative writing but poorly at arithmetic, while another may show the opposite pattern. Choosing the right model for a task requires careful, fair testing. This process is known as **evaluation**.

## 2. Objective

Design and carry out a fair comparison of **three open AI models** on a topic of the team's choice, measure their performance, and present the findings.

## 3. Scope of Work

The team will produce:

1. **A test set:** 10 questions (prompts) on a single chosen theme.
2. **A scoring rubric:** three criteria, each scored from 1 to 5.
3. **A scorecard:** a spreadsheet recording the score for every answer from every model.
4. **A presentation:** 4–5 slides summarising the method, results and conclusions.

Suggested themes: explaining concepts to a young audience, logic puzzles, arithmetic word problems, creative writing, responses in Indian languages, factual accuracy, or explaining short pieces of code.

## 4. Key Terms

| Term | Meaning |
|---|---|
| AI model | The underlying system that generates a chatbot's responses. |
| Open (open-weight) model | An AI model that is publicly available to download and use at no cost. |
| Prompt | The question or instruction given to the AI. |
| Rubric | A defined set of criteria used to assign scores consistently. |
| Evaluation | The process of testing an AI model to measure its quality. |

## 5. Requirements

- A laptop with a web browser
- **HuggingChat** (huggingface.co/chat): free access to several open models
- **LMArena** (lmarena.ai): side-by-side comparison of two models
- Google Sheets (or equivalent) for the scorecard, and Google Slides (or equivalent) for the presentation

## 6. Approach

| Step | Activity | Suggested time |
|---|---|---|
| 1 | Explore the tools and select a theme | 20 min |
| 2 | Write 10 test questions and define the rubric | 30 min |
| 3 | Run all 10 questions on all 3 models; record scores and capture screenshots | 70 min |
| 4 | Total the scores and identify patterns, strengths and weaknesses | 30 min |
| 5 | Prepare the presentation | 30 min |

**Fair testing rules:**
- Use the identical question for every model.
- Start a new conversation for each question.
- Where possible, have two team members score each answer independently and average the results.

## 7. Expected Deliverables

At the final demonstration, the team must present:

- [ ] The completed scorecard (10 questions × 3 models, with rubric scores)
- [ ] The overall result, with a simple chart
- [ ] At least one example of a notable model error, with a screenshot
- [ ] At least one unexpected finding
- [ ] A live comparison: one question suggested by the audience, answered by two models, with the audience voting on the better response

**Presentation time:** 3 minutes, followed by 1 minute of questions.

## 8. Optional Extensions

- Ask the same question several times and assess how consistent each model is.
- Compare a smaller and a larger model from the same family (for example, Llama 8B and Llama 70B).
- Test the models in one or more Indian languages.
