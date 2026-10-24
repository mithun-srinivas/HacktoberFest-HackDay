# Presenter Notes — Open Model Evaluation

**Target length:** 5 minutes plus live demo. **Date:** 24 October 2026.

## Opening (30 seconds)
We selected four open-weight models available through browser playgrounds: gpt-oss-20b, gpt-oss-120b, Qwen 3.8 27B Preview, and Gemma 4 31B. The goal is not to declare a universal best model; it is to compare models against our intended tasks using the same prompts and a consistent scoring rubric.

## Method (45 seconds)
The planned evaluation has 25 prompts across reasoning/math, factual accuracy, instruction following, coding, and Indian languages. Four scores are assigned per answer: correctness, instruction following, clarity and honesty, each from 1 to 5, for a total of 20. A fair run uses the same prompt, system instruction and temperature, a fresh chat per prompt, and two independent scorers who reconcile their ratings.

## Model facts (45 seconds)
OpenAI’s gpt-oss models use MoE architecture and Apache 2.0 licensing subject to the usage policy. Qwen 3.8 27B is a dense multimodal model under Apache 2.0; its native context specification differs from Groq’s hosted limit. Gemma 4 31B is a dense 30.7B model under Apache 2.0 with a 256K documented context and broad family multilingual capabilities. Model specs guide the test but do not replace our own results.

## Results (60 seconds)
In the work log available for this report, 13 of 100 intended model-prompt runs have complete scores. All 13 are reasoning/math. The recorded averages are 20.00 for gpt-oss-120b (n=4), 20.00 for Gemma 4 31B (n=2), 19.75 for gpt-oss-20b (n=4), and 19.67 for Qwen 3.8 27B (n=3). All four models answered Prompt 1 and Prompt 4 correctly. On Prompt 2, gpt-oss-20b and Qwen had minor clarity/formatting deductions even though the calculation was right. These small differences are not enough for a final ranking.

## Recommendations (60 seconds)
For a student help desk, pilot gpt-oss-120b and gpt-oss-20b with policy-grounded campus FAQs and safety checks. For coding, compare Qwen 3.8 27B and gpt-oss-120b by executing the same tests. For Indian-language users, compare Gemma 4 and Qwen with fluent human reviewers in Hindi and another target language. These are documentation-based pilots, not empirical winners from the current score sample.

## Live demo (60 seconds)
Ask the audience for a prompt or use: “Write a Python function that returns the second-largest distinct number in a list. Explain how it handles duplicates.” Run it on gpt-oss-120b and Qwen 3.8 27B using matched settings and fresh chats. Test duplicates, negatives and lists with fewer than two distinct values. Score each model independently on the four criteria, then discuss the evidence and any limitation.

## Closing (20 seconds)
The current evidence shows all models handle simple arithmetic and reasoning items well. To make a defensible recommendation, we must finish the 100 planned runs, record the real playground settings, preserve outputs, and complete independent scoring. A blank result is missing evidence, not zero.

## Important accuracy note for the presenters
Do not say the complete benchmark is finished. The report/workbook bundle is based on results available in this chat plus public documentation. The connected Google Sheet could not be read from here, and no one signed into the user's AI Studio or GroqCloud account. Keep the current scores labelled preliminary until the missing data is added.
