# Hacktoberfest Hack Day: Problem Statements (Summary)

**Theme:** Open-Source AI and Open-Weight Models

This document summarises all seven problem statements for organisers and judges. The full participant-facing version of each problem statement is in the [problem-statements/](problem-statements/README.md) folder.

Each team of 2–4 participants selects one problem statement. Each must end with a working demonstration.

| No. | Problem Statement | Level | Coding required | API key | Starter material |
|---|---|---|---|---|---|
| 1 | Open Model Showdown | Foundation | None | None | [Worksheet](worksheets/01_open_model_showdown.md) |
| 2 | Build-a-Bot | Foundation | None | None (free GroqCloud account) | [Worksheet](worksheets/02_build_a_bot.md) |
| 3 | Persona Chatbot | Beginner | Edit text and settings | Groq (free) | [Notebook](templates/03_persona_chatbot.ipynb) |
| 4 | Image Classifier | Beginner | Edit lists and settings | None | [Notebook](templates/04_image_classifier.ipynb) |
| 5 | Study Quiz Generator | Beginner–Intermediate | Edit prompts and small logic | Groq (free) | [Notebook](templates/05_study_quiz_generator.ipynb) |
| 6 | Document Question Answering | Intermediate | Read and modify a pipeline | Groq (free) | [Notebook](templates/06_document_question_answering.ipynb) |
| 7 | First-Issue Finder | Advanced | Web APIs and prompts | Groq (free); GitHub token optional | [Notebook](templates/07_first_issue_finder.ipynb) |

**Participant requirements:** a laptop with a web browser and a Google account (for Google Colab). Problems 3, 5, 6 and 7 also require a free API key from console.groq.com, a service that hosts open-weight models such as OpenAI's gpt-oss.

**Guidance for judges:** a smaller project that works and is clearly explained should be valued above a more ambitious project that does not work. Teams are expected to explain how the AI component works and where it fails.

---

## 1. Open Model Showdown

**Summary:** A structured, fair comparison of three open AI models on a theme chosen by the team.

**Work to be done:** The team defines 10 test prompts and a three-criterion scoring rubric, runs every prompt on three open-weight models, records the scores, and presents its conclusions.

**Tools:** HuggingChat (huggingface.co/chat), LMArena (lmarena.ai), Google Sheets, Google Slides.

**Expected deliverables:**
- A completed scorecard (10 prompts × 3 models)
- A presentation of the overall result, notable failures and unexpected findings
- A live comparison using a prompt suggested by the audience

**Optional extensions:** consistency testing, comparing model sizes, testing in Indian languages.

---

## 2. Build-a-Bot

**Summary:** Design, test and improve a custom AI assistant using a system prompt in the Groq Playground, without writing code.

**Work to be done:** The team builds an assistant in the Groq Playground for one defined purpose and audience, tests it against a written test plan, revises the system prompt over at least three versions, and carries out red-teaming (deliberate attempts to make it misbehave).

**Tools:** Groq Playground (console.groq.com/playground) only, and a shared document for recording each system prompt version.

**Expected deliverables:**
- A working assistant, demonstrated live in the Groq Playground
- A comparison of first-version and final-version responses
- Three red-teaming attempts and the corrections made

**Optional extensions:** few-shot examples, comparing models, temperature comparison, restricted-word testing.

> **Note for organisers:** the Groq Playground does not create shareable links or permanently save prompts. Teams demonstrate from their own laptop and keep their prompt versions in a shared document.

---

## 3. Persona Chatbot

**Summary:** Adapt a working chatbot web application into an assistant with an original, defined persona.

**Work to be done:** Starting from the provided example, the team defines a new persona, adds example questions, adjusts settings such as temperature, and optionally adds features.

**Tools:** Google Colab, Python, Gradio, Groq API (`openai/gpt-oss-20b`).

**Expected deliverables:**
- A chatbot available through a public link
- A persona that stays consistent across at least five exchanges
- An explanation of system prompts and temperature, with a demonstration

**Optional extensions:** persona selection menu, larger model comparison, AI-based response review.

---

## 4. Image Classifier

**Summary:** A web application that classifies photos into categories defined by the team, using an open-weight vision model without additional training.

**Work to be done:** The team selects a theme and labels, refines label wording to improve accuracy, and measures accuracy on a set of test images.

**Tools:** Google Colab, Python, Gradio, Hugging Face `transformers`, model `openai/clip-vit-base-patch32`. No API key is required.

**Expected deliverables:**
- A live demonstration using webcam or phone images
- Accuracy results on 10 test images, before and after refinement
- An explanation of zero-shot classification

**Optional extensions:** prompt templates, confidence thresholds, alternative models (SigLIP, CLIP Large), practical use cases.

---

## 5. Study Quiz Generator

**Summary:** A web application that converts class notes into an interactive multiple-choice quiz with scoring and explanations.

**Work to be done:** The team refines the question-generation prompt, which produces structured JSON output, adds difficulty control, and improves the quiz experience.

**Tools:** Google Colab, Python, Gradio, Groq API, JSON.

**Expected deliverables:**
- A live demonstration using real course notes
- Clearly differentiated difficulty levels
- An explanation of why structured (JSON) output is used

**Optional extensions:** additional question types, hints, AI-based answer verification, flashcard export.

---

## 6. Document Question Answering

**Summary:** A Retrieval-Augmented Generation (RAG) application that answers questions from an uploaded PDF, using only the document's content, with page citations.

**Work to be done:** The team works with a pipeline that splits the document into chunks, creates embeddings with an open-weight model, retrieves relevant passages, and generates a cited answer. Teams experiment with the pipeline parameters.

**Tools:** Google Colab, Python, Gradio, `pypdf`, `sentence-transformers` (`all-MiniLM-L6-v2`), Groq API.

**Expected deliverables:**
- A live demonstration with a real PDF and correct page citations
- Display of the retrieved passages
- A demonstration that the application declines to answer questions not covered by the document

**Optional extensions:** chunk-size experiments, multiple documents, conversation memory, a with-RAG versus without-RAG comparison.

---

## 7. First-Issue Finder

**Summary:** A tool that finds beginner-friendly issues in any GitHub repository and explains them in plain language.

**Work to be done:** The tool requests open issues from the GitHub REST API, preferring those labelled for beginners, and uses an open-weight model to produce a summary, difficulty rating, required skills and a first step for each.

**Tools:** Google Colab, Python, Gradio, `requests`, GitHub REST API, Groq API.

**Expected deliverables:**
- A live demonstration using a repository named by the audience
- Structured issue cards with summary, difficulty, skills and first step
- One issue selected by the team, with an outline of how they would approach it

**Optional extensions:** skill filtering, suitability ranking, draft assignment comments, repository summaries.
