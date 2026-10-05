# Problem Statement 6: Document Question Answering

| | |
|---|---|
| **Level** | Intermediate (read and modify a multi-step program) |
| **Team size** | 2–4 participants |
| **Starter code** | [templates/06_document_question_answering.ipynb](../templates/06_document_question_answering.ipynb) |

---

## 1. Background

AI chatbots have broad general knowledge, but they have no access to an institution's own documents, such as course syllabi, hostel regulations, or student handbooks. When asked about these documents, an AI may give an answer that sounds convincing but is false. This is known as **hallucination**.

A widely used solution is **Retrieval-Augmented Generation (RAG)**. The program first searches the document for the passages most relevant to the question. It then gives only those passages to the AI and instructs it to answer using that information alone.

## 2. Objective

Build a web application that answers questions about an uploaded PDF document, using **only the content of that document**, and cites the **page number** of each answer.

A complete working example with a sample course syllabus is provided. Teams improve it and test it with real documents.

## 3. Scope of Work

The completed application must:

1. Accept an uploaded PDF document.
2. Answer questions using only information found in the document.
3. Cite the page number for each answer, for example "(p. 2)".
4. Show the passages that were retrieved and given to the AI.
5. State clearly when the answer cannot be found in the document, rather than inventing one.

## 4. Key Terms

| Term | Meaning |
|---|---|
| RAG (Retrieval-Augmented Generation) | A method that first retrieves relevant information, then uses an AI to write an answer from it. |
| Chunk | A short section of the document. The document is divided into chunks for searching. |
| Embedding | A list of numbers that represents the meaning of a piece of text. Texts with similar meanings have similar embeddings. |
| Retrieval | Finding the chunks whose meaning is closest to the question. |
| Citation | A reference to where the information came from, such as a page number. |
| Hallucination | When an AI produces information that is false but presented as fact. |

## 5. Requirements

- A laptop with a web browser and a Google account
- The starter notebook, opened in Google Colab
- A free Groq API key from console.groq.com (instructions are included in the notebook). Without a key, the retrieval step still works in demonstration mode.
- A text-based PDF document for testing, such as a course syllabus or student handbook. Scanned image-only documents are not supported.

## 6. Approach

1. Open the notebook in Google Colab and run each cell in order (Shift + Enter). The notebook answers a sample question about the provided syllabus.
2. Study the four stages of the pipeline in the code: **splitting** the document into chunks, **creating embeddings**, **retrieving** relevant chunks, and **generating** the answer.
3. Run the "Launch the application" cell, upload a document, and ask questions.
4. Make changes at the points marked **STUDENT TODO** in the code:
   - **Level 1:** application name and example questions
   - **Level 2:** chunk size, number of retrieved chunks, and the AI's answering rules
   - **Level 3:** additional features, such as a minimum relevance threshold or support for multiple documents
5. Run at least one controlled experiment (for example, comparing different chunk sizes) and record the results.

## 7. Expected Deliverables

At the final demonstration, the team must present:

- [ ] A live demonstration: uploading a real PDF and answering three questions with correct page references
- [ ] An explanation of the RAG process, using the retrieved passages shown in the application
- [ ] A test with a question whose answer is not in the document, showing that the application declines to answer
- [ ] The results of at least one experiment (for example, the effect of chunk size on answer quality)


## 8. Optional Extensions

- Remove the instruction that limits answers to the document, and show the effect on accuracy.
- Show answers with and without RAG side by side.
- Support several uploaded documents at once.
- Add conversation memory to allow follow-up questions.
