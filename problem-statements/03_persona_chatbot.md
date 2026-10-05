# Problem Statement 3: Persona Chatbot

| | |
|---|---|
| **Level** | Beginner (modify text and settings in working starter code) |
| **Team size** | 2–4 participants |
| **Duration** | Approximately 3 hours |
| **Starter code** | [templates/03_persona_chatbot.ipynb](../templates/03_persona_chatbot.ipynb) |

---

## 1. Background

Most AI chatbots have the same neutral, general-purpose style. However, a chatbot's personality, tone and focus can be fully customised through written instructions, without changing the underlying AI model.

This project uses **Llama**, an open AI model released by Meta, accessed through a free service called Groq.

## 2. Objective

Adapt a working chatbot web application into a chatbot with an **original, clearly defined persona** that anyone can use from a public link.

A complete working example (a computer science tutor that explains concepts using everyday comparisons) is provided. Teams replace it with their own concept.

## 3. Scope of Work

The completed chatbot must:

1. Have an original name, personality, and area of focus defined by the team.
2. Respond consistently in the defined style and stay within its intended topic.
3. Show suggested example questions that users can select.
4. Be reachable through a public web link on both laptops and mobile phones.

Example concepts: a campus orientation guide, a history tutor with a distinctive voice, a study-planning assistant, or a subject-specific revision helper.

## 4. Key Terms

| Term | Meaning |
|---|---|
| Persona | The defined character, tone and style of the chatbot. |
| System prompt | Instructions given to the AI before every conversation. The persona is defined here. |
| Temperature | A setting that controls how varied the AI's responses are. Low values (around 0) give consistent responses; high values (around 1.5) give more varied and less predictable responses. |
| Llama | An open AI model released by Meta. |
| API key | A private access code that allows the program to use the AI service. It must not be shared. |
| Google Colab | A free, browser-based environment for running Python code. No installation is required. |

## 5. Requirements

- A laptop with a web browser and a Google account
- The starter notebook, opened in Google Colab
- A free Groq API key from console.groq.com (instructions are included in the notebook). The notebook runs in a demonstration mode until a key is added.

## 6. Approach

1. Open the notebook in Google Colab and run each cell in order (Shift + Enter). The example chatbot will respond immediately.
2. Define the team's persona: who the chatbot is, how it communicates, and what it helps with.
3. Make changes at the points marked **STUDENT TODO** in the code:
   - **Level 1:** name, persona, greeting message, and example questions (text changes only)
   - **Level 2:** temperature, visual theme, and choice of AI model
   - **Level 3:** additional features (suggestions are listed at the end of the notebook)
4. Run the "Launch the application" cell and open the public link on a mobile phone.
5. Test the chatbot with other participants and refine the persona based on the results.

After editing any cell, re-run that cell and then re-run the launch cell for the changes to take effect.

## 7. Expected Deliverables

At the final demonstration, the team must present:

- [ ] A working chatbot, available through a public link that the audience can open
- [ ] An original persona (not the provided example) that stays consistent for at least five exchanges
- [ ] A one-sentence explanation of what a **system prompt** is and what **temperature** controls, ideally shown by comparing the same question at temperature 0 and 1.5
- [ ] One example of an attempt to make the chatbot break character, and how the team addressed it

**Presentation time:** 3 minutes, followed by 1 minute of questions.

## 8. Optional Extensions

- Add a selection menu that lets users choose between several personas.
- Switch to a larger model (`llama-3.3-70b-versatile`) and compare the quality of responses.
- Require the chatbot to end each response with a follow-up question.
- Add a second AI step that reviews and rates each response for accuracy.
