# Problem Statement 7: First-Issue Finder

| | |
|---|---|
| **Level** | Advanced (work with external web APIs) |
| **Team size** | 2–4 participants |
| **Starter code** | [templates/07_first_issue_finder.ipynb](../templates/07_first_issue_finder.ipynb) |

---

## 1. Background

Hacktoberfest is an annual event, held every October, that encourages people to contribute to **open-source software**: software whose source code is publicly available for anyone to use and improve.

Open-source projects track their pending work on GitHub as **issues**. Many projects label tasks that suit newcomers as **"good first issue"**. However, these issues are often written in technical language that beginners find hard to understand, which discourages new contributors.

## 2. Objective

Build a tool that, given the name of any GitHub project, **finds beginner-friendly issues** and uses an AI model to **explain each one in plain language**: what the task involves, its difficulty, the skills required, and a suggested first step.

A complete working example is provided. Teams extend and improve it.

## 3. Scope of Work

The completed tool must:

1. Accept a GitHub project name (for example, `ollama/ollama`) or project URL.
2. Fetch open issues from GitHub in real time, preferring those labelled for beginners.
3. Use an AI model to produce, for each issue:
   - a plain-language summary
   - a difficulty rating (Easy, Medium or Hard)
   - the skills required
   - a recommended first step
4. Show each issue as a structured card with a link to the original issue.

## 4. Key Terms

| Term | Meaning |
|---|---|
| Open source | Software whose source code is publicly available to view, use and improve. |
| GitHub | A platform for hosting code and collaborating on software projects. |
| Repository | A single project on GitHub, written as `owner/project-name`. |
| Issue | A task, bug report, or feature request recorded in a GitHub project. |
| "Good first issue" | A label projects use to mark tasks suitable for new contributors. |
| API (Application Programming Interface) | A defined way for one program to request data or services from another. This tool uses two: GitHub (for issues) and Groq (for AI explanations). |
| JSON | A structured text format that programs can read easily. |

## 5. Requirements

- A laptop with a web browser and a Google account
- The starter notebook, opened in Google Colab
- A free Groq API key from console.groq.com (instructions are included in the notebook). Without a key, the tool still fetches real issues but does not generate explanations.
- Optional: a free GitHub access token, needed only if GitHub usage limits are reached (instructions are included in the notebook)

## 6. Approach

1. Open the notebook in Google Colab and run each cell in order (Shift + Enter). The notebook fetches and shows real issues from a sample project.
2. Study the two stages of the tool: requesting issues from the **GitHub API**, then requesting explanations from the **AI model**.
3. Run the "Launch the application" cell and test it with several projects.
4. Make changes at the points marked **STUDENT TODO** in the code:
   - **Level 1:** application name, default project, and example projects
   - **Level 2:** number of issues shown and the AI's explanation instructions
   - **Level 3:** additional features, such as filtering by skill or ranking by suitability for beginners
5. Use the completed tool to find an issue the team could realistically work on.

## 7. Expected Deliverables

At the final demonstration, the team must present:

- [ ] A live demonstration: a project named by the audience, with real issues found and explained
- [ ] Structured issue cards showing summary, difficulty, required skills and first step
- [ ] A one-sentence explanation of what an API is and how the tool combines two of them
- [ ] One issue selected by the team using the tool, with an outline of how they would approach it


## 8. Optional Extensions

- Add filtering by type or skill (for example, documentation or Python only).
- Have the AI assign each issue a suitability score from 1 to 10 and sort the results by it.
- Generate a draft comment requesting to be assigned to an issue.
- Show a short summary of the project, generated from its README file.
- Make a real contribution to an open-source project during Hacktoberfest.
