# Problem Statement 2: Build-a-Bot

| | |
|---|---|
| **Level** | Foundation (no coding required) |
| **Team size** | 2–4 participants |
| **Duration** | Approximately 3 hours |
| **Resources** | [Detailed worksheet](../worksheets/02_build_a_bot.md) |

---

## 1. Background

General-purpose AI chatbots are designed to answer any kind of question. As a result, they are often not well suited to a specific job or audience.

An AI's behaviour can be shaped by giving it written instructions before the conversation begins. These instructions are called a **system prompt**. They set the assistant's role, tone, and rules. Organisations use this technique to build customer-support assistants, tutoring tools, and similar applications.

## 2. Objective

Design, test and improve a **custom AI assistant** for one clearly defined purpose and audience, without writing any code.

## 3. Scope of Work

The team will produce:

1. **A custom AI assistant** with a name, a defined role and audience, and a set of behavioural rules. Examples: a campus orientation guide for first-year students, a cooking assistant for hostel residents, or a programming tutor that provides hints rather than full solutions.
2. **A test plan:** at least 10 test questions, covering typical, difficult, and off-topic requests.
3. **A version history:** at least three versions of the system prompt, recording the changes made and the effect of each.
4. **A robustness review:** at least three attempts to make the assistant behave incorrectly, and the corrections made in response.

## 4. Key Terms

| Term | Meaning |
|---|---|
| Assistant / chatbot | An AI application that users interact with through text conversation. |
| System prompt | Instructions given to the AI before every conversation, defining its role and rules. |
| Persona | The defined character, tone and style of the assistant. |
| Red-teaming | Deliberately trying to make a system fail, in order to find and fix weaknesses. |
| Open model | A publicly available AI model, such as Llama or Qwen, on which the assistant runs. |

## 5. Requirements

- A laptop with a web browser
- A free Hugging Face account (huggingface.co/join)
- **HuggingChat Assistants** (huggingface.co/chat/assistants)
  - If this service is unavailable, the organisers will direct teams to the **Groq Playground** (console.groq.com/playground) as an alternative.
- A shared document for recording versions and test results

## 6. Approach

| Step | Activity | Suggested time |
|---|---|---|
| 1 | Define the assistant's purpose and target audience | 20 min |
| 2 | Write the first version of the system prompt and create the assistant | 30 min |
| 3 | Run the test plan and record the results | 30 min |
| 4 | Revise the system prompt, re-test, and carry out red-teaming | 60 min |
| 5 | Prepare the presentation | 30 min |

A system prompt template is provided in the detailed worksheet.

## 7. Expected Deliverables

At the final demonstration, the team must present:

- [ ] A working assistant that the judges can access (via a link or QR code)
- [ ] A comparison of responses from the first and final versions to the same question
- [ ] Three red-teaming attempts and the corrections made
- [ ] One key lesson learned about writing instructions for AI

**Presentation time:** 3 minutes, followed by 1 minute of questions.

## 8. Optional Extensions

- Include an example conversation in the system prompt and assess its effect on response style.
- Apply the same system prompt to a different model and compare how well each follows the rules.
- Define a restricted word the assistant must never use, and invite the audience to test it.
