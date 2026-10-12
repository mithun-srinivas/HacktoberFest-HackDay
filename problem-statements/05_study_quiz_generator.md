# Problem Statement 5: Study Quiz Generator

| | |
|---|---|
| **Level** | Beginner–Intermediate (modify AI instructions and small amounts of program logic) |
| **Team size** | 2–4 participants |
| **Starter code** | [templates/05_study_quiz_generator.ipynb](../templates/05_study_quiz_generator.ipynb) |

---

## 1. Background

Self-testing is one of the most effective ways to prepare for an examination. However, writing practice questions by hand takes a lot of time.

AI models can write quiz questions from study material. They normally respond in ordinary sentences, which a program cannot reliably process. To solve this, the AI is instructed to respond in **JSON**, a structured data format. The application can then read the response and turn it into interactive quiz elements. This is a common technique in real-world AI applications.

## 2. Objective

Build a web application that turns a student's class notes into an **interactive multiple-choice quiz**, with automatic scoring and explanations.

A complete working example is provided. Teams improve and customise it.

## 3. Scope of Work

The completed application must:

1. Accept pasted class notes on any subject.
2. Let the user choose the difficulty level (easy, medium, hard) and the number of questions.
3. Generate multiple-choice questions, each with four options.
4. Check the user's answers, show a score, and explain each correct answer.

## 4. Key Terms

| Term | Meaning |
|---|---|
| Prompt | The instructions given to the AI. Here, the prompt defines how the questions should be written. |
| JSON | A structured text format that programs can read easily, for example `{"question": "...", "options": [...]}`. |
| Multiple-choice question | A question with several options, exactly one of which is correct. |
| gpt-oss | An open-weight AI model released by OpenAI, used here to generate the questions. |
| API key | A private access code that allows the program to use the AI service. It must not be shared. |

## 5. Requirements

- A laptop with a web browser and a Google account
- The starter notebook, opened in Google Colab
- A free Groq API key from console.groq.com (instructions are included in the notebook). The notebook runs in a demonstration mode with a sample quiz until a key is added.
- Notes from at least one real course, for use in the final demonstration

## 6. Approach

1. Open the notebook in Google Colab and run each cell in order (Shift + Enter). A sample quiz will be shown.
2. Run the "Launch the application" cell and generate and complete a quiz.
3. Make changes at the points marked **STUDENT TODO** in the code:
   - **Level 1:** application name and sample notes
   - **Level 2:** the AI's question-writing instructions and the score feedback messages
   - **Level 3:** additional features, such as true/false questions or hints
4. Test with real course notes. Check that the questions are accurate and that the difficulty levels differ meaningfully.

When editing the AI's instructions, do not remove the JSON format section. The application depends on it.

## 7. Expected Deliverables

At the final demonstration, the team must present:

- [ ] A working, customised quiz application
- [ ] A live demonstration: generating and completing a quiz from real course notes
- [ ] Evidence that the difficulty levels produce clearly different questions
- [ ] A one-sentence explanation of why the AI is asked to respond in JSON
- [ ] At least one example of an inaccurate question or answer produced by the AI, and how the team addressed it


## 8. Optional Extensions

- Add true/false questions.
- Add a hint for each question.
- Randomise the order of questions and options.
- Add a second AI step that checks each answer against the source notes.
- Export the quiz as a set of flashcards.
