# Theme 1: Open Model Evaluation

| | |
|---|---|
| **Level** | Beginner (no coding required) |
| **Team size** | 4–6 participants |
| **Platforms** | Groq Playground (console.groq.com/playground) and Google AI Studio (aistudio.google.com) |
| **Resources** | [Evaluation worksheet](../worksheets/01_model_evaluation.md) |

---

## 1. Background

Open-weight AI models are models whose weights are publicly released, so anyone can download, run, study and build on them. Organisations such as Google, OpenAI and Alibaba release open-weight models under licences such as Apache 2.0.

Choosing a model for a real application means understanding both **what the model is** (its size, design, licence and stated limitations) and **how well it performs** on the tasks that matter. Published benchmarks give one view. Careful, hands-on testing by the people who will use the model gives another. This process is called **model evaluation**.

## 2. Objective

Research and evaluate a set of open-weight models, using the free web playgrounds and the models' published documentation, and present evidence-based findings and recommendations.

## 3. Models to evaluate

Evaluate **at least four** of the following models, including at least one from each platform.

| Model | Developer | Platform | Model card |
|---|---|---|---|
| gpt-oss-20b | OpenAI | Groq Playground | https://huggingface.co/openai/gpt-oss-20b |
| gpt-oss-120b | OpenAI | Groq Playground | https://huggingface.co/openai/gpt-oss-120b |
| Qwen 3.8 27B (preview) | Alibaba | Groq Playground | https://huggingface.co/Qwen/Qwen3.8-27B |
| Gemma 4 31B | Google | Google AI Studio | https://huggingface.co/google/gemma-4-31B-it |
| Gemma 4 26B A4B | Google | Google AI Studio | https://huggingface.co/google/gemma-4-26B-A4B-it |

Model availability on each platform can change. If a listed model is unavailable, select another open-weight model offered on the same platform and record the substitution.

## 4. Scope of Work

The team will:

1. **Research each model** using its model card and the developer's documentation. Record the developer, parameter count, architecture, context length, licence, release date, intended uses and stated limitations.
2. **Design an evaluation:** at least **25 test prompts** across at least **five categories** (for example reasoning and mathematics, factual accuracy, instruction following, coding, Indian languages, and safety), with a written scoring rubric.
3. **Run the evaluation** on every selected model under the same conditions, and record all scores.
4. **Analyse the results:** compare the models overall and by category, identify strengths, weaknesses and failure patterns, and relate the findings to what the model documentation states.
5. **Recommend** which model suits which kind of application, with justification.

## 5. Key Terms

| Term | Meaning |
|---|---|
| Open-weight model | A model whose trained weights are publicly available to download and use. |
| Model card | The documentation published with a model, describing its design, training, intended use and limitations. |
| Parameters | The learned values inside a model. Parameter count is a common measure of model size. |
| Mixture of Experts (MoE) | A design in which only part of the model is active for each token. "26B A4B" means 26 billion parameters in total, with about 4 billion active. |
| Context length | The maximum amount of text the model can consider at once. |
| System prompt | Instructions given to the model before the conversation, shaping its behaviour. |
| Temperature | A setting that controls how varied the model's responses are. |
| Hallucination | A response that presents false information as fact. |

## 6. Requirements

- A laptop with a web browser
- A free GroqCloud account (console.groq.com) and a Google account (for Google AI Studio)
- A shared spreadsheet for the scorecard and a slide deck for the presentation

## 7. Approach

| Step | Activity |
|---|---|
| 1 | Divide the models among team members and complete the model fact sheet for each |
| 2 | Agree the evaluation categories, test prompts and scoring rubric |
| 3 | Run every prompt on every model with the same settings, and record the scores and notable responses |
| 4 | Analyse the results by model and by category |
| 5 | Prepare the presentation and the live demonstration |

**Fair testing rules:**
- Use the identical prompt, system prompt and temperature for every model.
- Start a new conversation for each prompt.
- Have at least two team members score each response independently, then agree a final score.

## 8. Expected Deliverables

At the showcase, the team must present:

- [ ] A **model fact sheet** comparing the selected models (from the model cards)
- [ ] The completed **scorecard**, with results by model and by category
- [ ] An **analysis** of strengths, weaknesses and failure patterns, with examples
- [ ] A **recommendation** of which model to use for which kind of application, with justification
- [ ] A **live demonstration**: one prompt suggested by the audience, run on two models, with the results discussed

## 9. Good to Have (bonus points)

- **Settings study:** measure how temperature or the system prompt changes results on the same prompts.
- **Consistency study:** run selected prompts several times and measure how often each model gives the same answer.
- **Speed and size:** record response speed where the platform shows it, and discuss the trade-off between model size, speed and quality.
- **Comparison with published results:** compare your findings with the LMArena leaderboard (lmarena.ai/leaderboard) or benchmarks in the model cards, and explain any differences.
- **Licence review:** summarise what each licence permits, for example commercial use and modification.
- **Multilingual depth:** a dedicated evaluation in two or more Indian languages.
