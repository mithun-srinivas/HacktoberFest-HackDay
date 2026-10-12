# Hacktoberfest Hack Day: Problem Statements

**Theme:** Open-Source AI and Open-Weight Models

Each team of 2–4 participants selects **one** of the problem statements below. Every project must end with a working demonstration.

Participants with no prior coding experience are encouraged to choose Problem 1, 2 or 3.

| No. | Problem Statement | Level | Coding required | Account or key needed | Full details | Starter material |
|---|---|---|---|---|---|---|
| 1 | Open Model Showdown | Foundation | None | None | [Problem statement](problem-statements/01_open_model_showdown.md) | [Worksheet](worksheets/01_open_model_showdown.md) |
| 2 | Build-a-Bot | Foundation | None | Free GroqCloud account | [Problem statement](problem-statements/02_build_a_bot.md) | [Worksheet](worksheets/02_build_a_bot.md) |
| 3 | Persona Chatbot | Beginner | Edit text and settings | Free Groq API key | [Problem statement](problem-statements/03_persona_chatbot.md) | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/03_persona_chatbot.ipynb) |
| 4 | Image Classifier | Beginner | Edit lists and settings | None | [Problem statement](problem-statements/04_image_classifier.md) | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/04_image_classifier.ipynb) |
| 5 | Document Question Answering | Intermediate | Read and modify a short program | Free Groq API key | [Problem statement](problem-statements/05_document_question_answering.md) | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/05_document_question_answering.ipynb) |

### Levels

| Level | What it involves |
|---|---|
| Foundation | No coding. Work is done using free web tools. |
| Beginner | Modify text and settings in starter code that already works. |
| Intermediate | Read and modify a multi-step program. |

**All teams need:** a laptop with a web browser and a Google account. A free Groq account or API key can be created at console.groq.com; instructions are included in the worksheet or notebook.

---

## 1. Open Model Showdown

**Level:** Foundation (no coding)

**What you will do:** Compare three free, open AI models in a fair test. Write 10 questions on a theme of your choice, score every answer using a simple rubric, and present which model performed best and why.

**Tools:** HuggingChat (huggingface.co/chat), LMArena (lmarena.ai), Google Sheets, Google Slides.

**What you will present:**
- Your completed scorecard (10 questions × 3 models)
- The overall result, notable errors, and one unexpected finding
- A live comparison using a question suggested by the audience

---

## 2. Build-a-Bot

**Level:** Foundation (no coding)

**What you will do:** Design your own AI assistant for one specific purpose and audience by writing its instructions (the system prompt) in the Groq Playground. Test it, improve it over at least three versions, and try to make it fail so that you can fix its weaknesses.

**Tools:** Groq Playground (console.groq.com/playground) and a shared document for recording each version.

**What you will present:**
- Your assistant, demonstrated live in the Groq Playground
- Responses from the first and final versions to the same question
- Three attempts to make the assistant fail, and how you corrected them

---

## 3. Persona Chatbot

**Level:** Beginner

**What you will do:** Start from a chatbot web application that already works and turn it into a chatbot with your own character and purpose. Change its instructions, example questions and settings, then share it through a public link.

**Tools:** Google Colab, Python, Gradio, Groq API (open-weight model `openai/gpt-oss-20b`).

**What you will present:**
- Your chatbot, available through a public link that the audience can open
- A persona that stays consistent for at least five exchanges
- A short explanation of what a system prompt and temperature are, with a demonstration

---

## 4. Image Classifier

**Level:** Beginner

**What you will do:** Build a web application that identifies what is in a photo, choosing from a list of categories that you define. The open-weight model runs inside Google Colab, so no API key is needed. Improve the category wording and measure how accurate the application is.

**Tools:** Google Colab, Python, Gradio, Hugging Face `transformers`, open-weight model CLIP.

**What you will present:**
- A live demonstration using a webcam or phone photo
- Accuracy results on 10 test photos, before and after your improvements
- A short explanation of zero-shot classification

---

## 5. Document Question Answering

**Level:** Intermediate

**What you will do:** Build a web application that answers questions about an uploaded PDF (such as a course syllabus) using only the content of that document, and shows the page number for each answer. This technique is called Retrieval-Augmented Generation (RAG).

**Tools:** Google Colab, Python, Gradio, `pypdf`, `sentence-transformers`, Groq API.

**What you will present:**
- A live demonstration with a real PDF and correct page references
- The passages the application retrieved, used to explain how RAG works
- A question that is not covered by the document, which the application declines to answer
