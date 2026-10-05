# Hacktoberfest Hack Day: Open-Source AI Starter Kit

This kit supports a one-day hack day for first-year college students on the theme of **open-source AI and open-weight models**. All coding projects run in **Google Colab** (browser only, no installation), and all tools and models are **free to use**. No paid API keys are required.

## Contents

| Item | Audience | Description |
|---|---|---|
| [problem-statements/](problem-statements/README.md) | Participants | One document per problem statement: background, objective, scope, key terms, requirements, approach and expected deliverables |
| [PROBLEM_STATEMENTS.md](PROBLEM_STATEMENTS.md) | Organisers and judges | All seven problem statements summarised in a single document |
| [ORGANIZER_GUIDE.md](ORGANIZER_GUIDE.md) | Organisers and mentors | Event schedule, preparation checklist, mentor reference and judging criteria |
| [worksheets/01_open_model_showdown.md](worksheets/01_open_model_showdown.md) | Participants (Problem 1) | Step-by-step worksheet for the no-code model evaluation project |
| [worksheets/02_build_a_bot.md](worksheets/02_build_a_bot.md) | Participants (Problem 2) | Step-by-step worksheet for the no-code assistant design project |
| [templates/03_persona_chatbot.ipynb](templates/03_persona_chatbot.ipynb) | Participants (Problem 3) | Starter notebook: chatbot with a configurable persona |
| [templates/04_image_classifier.ipynb](templates/04_image_classifier.ipynb) | Participants (Problem 4) | Starter notebook: zero-shot image classifier (no API key required) |
| [templates/05_study_quiz_generator.ipynb](templates/05_study_quiz_generator.ipynb) | Participants (Problem 5) | Starter notebook: quiz generator using structured JSON output |
| [templates/06_document_question_answering.ipynb](templates/06_document_question_answering.ipynb) | Participants (Problem 6) | Starter notebook: document question answering (RAG) with page citations |
| [templates/07_first_issue_finder.ipynb](templates/07_first_issue_finder.ipynb) | Participants (Problem 7) | Starter notebook: GitHub issue finder with AI-generated explanations |

## Open a starter notebook in Google Colab

| Problem | Link |
|---|---|
| 3. Persona Chatbot | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/03_persona_chatbot.ipynb) |
| 4. Image Classifier | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/04_image_classifier.ipynb) |
| 5. Study Quiz Generator | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/05_study_quiz_generator.ipynb) |
| 6. Document Question Answering | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/06_document_question_answering.ipynb) |
| 7. First-Issue Finder | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/07_first_issue_finder.ipynb) |

## Getting started (participants)

1. Open the notebook for your problem statement in Google Colab using the links above.
2. Select **File → Save a copy in Drive** so that your changes are saved.
3. For Problems 3, 5, 6 and 7, create a free API key at **console.groq.com** and add it in the Colab **Secrets** panel under the name `GROQ_API_KEY`. Until a key is added, the notebook runs in demonstration mode.
4. Run the cells in order from top to bottom (**Shift + Enter**). The application appears at the end of the notebook, together with a public link.
5. Make your changes at the points marked **STUDENT TODO**.

## Models used

| Model | Developer | Used in | Hosted on |
|---|---|---|---|
| Llama 3.1 8B / Llama 3.3 70B | Meta | Problems 3, 5, 6, 7 | Groq (free tier) |
| gpt-oss 20B (optional alternative) | OpenAI | Any LLM-based problem | Groq (free tier) |
| CLIP ViT-B/32 | OpenAI | Problem 4 | Google Colab |
| all-MiniLM-L6-v2 | sentence-transformers | Problem 6 | Google Colab |
