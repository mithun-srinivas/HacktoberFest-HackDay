# Hacktoberfest Hack Day: Themes

**Theme:** Open-Source AI and Open-Weight Models

Each team of **4–6 participants** selects **one** of the three themes below. Every project must end with a presentation and a live demonstration at the showcase.

| No. | Theme | Level | Coding required | Platform | Full details | Starter material |
|---|---|---|---|---|---|---|
| 1 | Open Model Evaluation | Beginner | None | Groq Playground, Google AI Studio | [Problem statement](problem-statements/01_model_evaluation.md) | [Worksheet](worksheets/01_model_evaluation.md) |
| 2 | RAG Application with Gemma | Intermediate | Python | Google Colab (no GPU), Google AI Studio API | [Problem statement](problem-statements/02_rag_application.md) | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/02_rag_starter_kit.ipynb) |
| 3 | Fine-Tuning Gemma | Advanced | Python | Google Colab (T4 GPU), Unsloth | [Problem statement](problem-statements/03_fine_tuning.md) | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/03_fine_tuning_starter_kit.ipynb) |

Themes 2 and 3 each offer **two problem statements**. Teams choosing these themes select one problem statement within the theme.

**All teams need:** a laptop with a web browser and a Google account. Theme 1 also requires a free GroqCloud account (console.groq.com). Theme 2 requires a free Google AI Studio API key (aistudio.google.com/apikey).

---

## 1. Open Model Evaluation

**Level:** Beginner (no coding)

**What you will do:** Research and evaluate at least four open-weight models (OpenAI gpt-oss, Alibaba Qwen and Google Gemma 4) using the Groq Playground and Google AI Studio. Read each model's documentation, design a structured evaluation across several categories, score the models fairly, and recommend which model suits which application.

**What you will present:**
- A model fact sheet and a completed scorecard
- An analysis of strengths, weaknesses and failure patterns
- Recommendations, and a live comparison using a prompt from the audience

---

## 2. RAG Application with Gemma

**Level:** Intermediate

**What you will do:** Start from a working Retrieval-Augmented Generation (RAG) application built on Google's open-weight Gemma 4 model, accessed through the free Google AI Studio API from Google Colab. Adapt and extend it so that it answers questions from documents with citations and declines questions the documents do not cover.

**Problem statements (choose one):**
- **2A. Campus Regulations Assistant:** answer students' questions about college rules, using official handbooks and regulations, with document and page citations.
- **2B. Open-Source Contributor Guide:** help newcomers start contributing to a real open-source project, using its README, contributing guide and other documentation.

**What you will present:**
- A working application demonstrated with your own documents
- An evaluation of answer quality on a test set of questions
- An explanation of your pipeline and design decisions, with bonus features where completed

---

## 3. Fine-Tuning Gemma

**Level:** Advanced

**What you will do:** Measure the plain Gemma 4 model on your chosen problem, fine-tune it with LoRA using Unsloth on a free Colab GPU, build an application around the fine-tuned model, and compare the plain and fine-tuned models.

**Problem statements (choose one):**
- **3A. Teach Gemma to Understand Code-Mixed Regional Languages:** fine-tune Gemma to convert between English, regional-script text and informal romanized text in Kannada or Hindi, using AI4Bharat IndicCMix (requires a free Hugging Face account).
- **3B. Extract Information from Receipts:** fine-tune Gemma on images to extract the merchant, date, address and total from receipt images, using ICDAR 2019 SROIE.

**What you will present:**
- A fine-tuned model, with the dataset and training settings documented
- A comparative analysis of the plain and fine-tuned models on the same test set
- A working application built around the fine-tuned model
