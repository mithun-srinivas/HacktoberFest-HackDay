# Theme 2: RAG Application with Gemma

| | |
|---|---|
| **Level** | Intermediate |
| **Team size** | 4–6 participants |
| **Platform** | Google Colab (no GPU required) and a free Google AI Studio API key |
| **Starter kit** | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/02_rag_starter_kit.ipynb) |

---

## 1. Background

Language models have broad general knowledge but no access to private or specialised documents, such as institutional regulations, course material or project documentation. When asked about such documents, a model may produce answers that sound convincing but are false.

**Retrieval-Augmented Generation (RAG)** addresses this. The application first retrieves the passages of a document most relevant to a question, then gives only those passages to the model and instructs it to answer from them, with citations.

## 2. Objective

Using the starter kit, build a RAG application with Google's open-weight **Gemma 4** model for one of the two problem statements below. The application must answer accurately from the provided documents, cite its sources, and decline questions the documents do not cover.

## 3. What is Provided

The starter kit is a complete, working Colab notebook containing:

- **Gemma 4** (`gemma-4-26b-a4b-it`), accessed through the free Google AI Studio API
- An open-weight embedding model (`all-MiniLM-L6-v2`) running in the notebook
- A RAG pipeline: PDF reading, chunking, embedding, retrieval and cited answer generation
- A Gradio web application with a public link, which displays the retrieved passages
- A sample document, so that the application works immediately

## 4. Problem Statements (choose one)

### 2A. Campus Regulations Assistant

**Problem statement:** Students often cannot find clear answers about college rules, because the information is spread across long handbooks and regulation documents. Build an assistant that answers students' questions about college regulations accurately, using only the official documents.

**Data:** publicly available regulations from your own college or university, for example the student handbook, examination regulations, hostel rules or library policies (at least two documents).

**The application must answer questions such as:**
- "What is the minimum attendance required to sit the end-semester examination?"
- "Can I apply for a re-evaluation, and what is the deadline?"
- "What are the hostel visiting hours?"

**Expected output:** an assistant that cites the document name and page for every answer, and declines questions the documents do not cover, suggesting whom to contact instead.

### 2B. Open-Source Contributor Guide

**Problem statement:** First-time contributors often give up before making a contribution, because project documentation is long and scattered across many files. Build an assistant that helps newcomers start contributing to a real open-source project during Hacktoberfest.

**Data:** the contributor documentation of a real open-source project of your choice, for example its README, CONTRIBUTING guide, code of conduct and development set-up guide.

**The application must answer questions such as:**
- "How do I set up the project on my computer?"
- "What is the process for submitting a pull request?"
- "Which coding style rules must I follow?"

**Expected output:** an assistant that reads Markdown (`.md`) and plain-text files in addition to PDFs (an extension to the starter kit), and cites the source file for every answer.

### For either problem statement, the team will:
1. Collect and prepare the documents.
2. Adapt the pipeline, prompt and settings to the problem statement.
3. Build an application suited to the intended users.
4. Create a test set of questions with expected answers, and use it to measure the application's quality.

## 5. Key Terms

| Term | Meaning |
|---|---|
| RAG | Retrieval-Augmented Generation: retrieving relevant information, then generating an answer from it. |
| Chunk | A short section of a document. Documents are divided into chunks for retrieval. |
| Embedding | A list of numbers that represents the meaning of a piece of text. |
| Retrieval | Finding the chunks whose embeddings are closest to the question's embedding. |
| Top-k | The number of retrieved chunks given to the model for each question. |
| Hallucination | A response that presents false information as fact. |
| Gemma 4 | Google's open-weight model family, released under the Apache 2.0 licence. |

## 6. Requirements

- A laptop with a web browser and a Google account
- The starter kit, opened in Google Colab (the default CPU runtime is sufficient)
- A free Google AI Studio API key from aistudio.google.com/apikey (one per team member is recommended, to share the usage limits)
- Text-based PDF documents relevant to the use case (scanned image-only documents are not supported)

## 7. Expected Deliverables

At the showcase, the team must present:

- [ ] A **working application** for the use case, demonstrated live with the team's own documents
- [ ] **Cited answers:** answers that reference the source page or document
- [ ] **Transparency:** the retrieved passages shown for each answer
- [ ] **Refusal test:** questions not covered by the documents, which the application declines to answer
- [ ] **Evaluation:** a test set of at least 15 questions, with the proportion answered correctly, and an explanation of the main failure cases
- [ ] **Explanation** of the pipeline and of the design decisions made (for example chunk size and top-k)

## 8. Good to Have (bonus points)

- **Experiments:** compare chunk sizes, top-k values or embedding models on the test set, and present the results.
- **RAG versus no RAG:** show answers to the same questions with and without retrieval.
- **Multiple documents:** support several documents, with the document name in each citation.
- **Relevance threshold:** decline to answer when no passage is sufficiently relevant.
- **Conversation memory:** support follow-up questions.
- **Model comparison:** compare Gemma 4 26B A4B with Gemma 4 31B on answer quality and speed.
- **Improved retrieval:** for example, re-ranking retrieved passages or combining keyword and semantic search.
- **User experience:** a polished interface designed for the intended users.
- **2A only:** detect when two documents give conflicting information, and show both passages.
- **2B only:** a "where do I start?" feature that produces a step-by-step onboarding checklist from the documents.
