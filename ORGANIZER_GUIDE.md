# Organiser and Mentor Guide: Hacktoberfest Hack Day

This guide covers the event schedule, preparation checklist, distribution of starter materials, a mentor reference, and judging criteria.

---

## 1. Event schedule (09:00–18:00, 4.5 hours of build time)

| Time | Session | Notes |
|---|---|---|
| 09:00 – 09:30 | Registration and network access | Ask participants to open colab.research.google.com and sign in while waiting, so account problems are found early. |
| 09:30 – 10:15 | Opening session: introduction to open-source AI (20 minutes) and overview of the problem statements | Include one short live demonstration, such as changing the persona in the Persona Chatbot notebook. |
| 10:15 – 10:45 | Team formation, problem selection and setup | Each team runs the first cells of its notebook and confirms output before Sprint 1 begins. Groq API keys are created during this session. |
| 10:45 – 13:00 | **Sprint 1** (2 hours 15 minutes) | Target: Level 1 changes complete and the application running with the team's own concept. |
| 13:00 – 13:45 | Lunch | A one-minute progress check-in per team at the end of lunch. |
| 13:45 – 16:00 | **Sprint 2** (2 hours 15 minutes) | Target: Level 2 and Level 3 changes, and the experiment required for the demonstration. |
| 16:00 – 16:30 | Demonstration preparation | Development stops at 16:00. Teams prepare slides, test public links on a mobile device, and prepare backup screenshots. |
| 16:30 – 17:30 | Demonstrations (3 minutes per team, plus 1 minute of questions) | For more than 15 teams, use two parallel rooms or an exhibition format. |
| 17:30 – 18:00 | Judging, awards and closing | Close with information on contributing to open-source projects during Hacktoberfest. |

---

## 2. Preparation checklist

### Two weeks before the event
- [ ] **Host the starter materials** using one of the following methods:
  - **GitHub (recommended):** the materials are published at https://github.com/mithun-srinivas/HacktoberFest-HackDay. Participants can open each notebook directly in Colab using the links in the repository README (for example, `https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/03_persona_chatbot.ipynb`). Share these links on a slide or as QR codes. The repository must remain public for these links to work.
  - **Google Drive:** upload the `templates/` folder to a shared Drive folder. Participants open each notebook with Google Colaboratory and select **File → Save a copy in Drive**.
- [ ] Tell participants to bring a laptop and to confirm they can sign in to a Google account. Some institutional Google Workspace accounts restrict Colab, so participants should test access in advance or use a personal account.
- [ ] Recruit mentors at a ratio of about one mentor per three to four teams, with one or two mentors assigned to the no-code teams.

### One week before the event
- [ ] **Test every notebook in Google Colab with a valid Groq API key.** Run all cells in order, launch each application, and open the public link on a mobile device.
- [ ] Confirm at https://console.groq.com/docs/models that `llama-3.1-8b-instant` is still available. If it has been retired, update the `MODEL` setting in each notebook (one line per notebook).
- [ ] Confirm that HuggingChat Assistants (huggingface.co/chat/assistants) is available for Problem 2. If it is not, the worksheet describes the Groq Playground alternative.
- [ ] Test the venue network with Google Colab and a `*.gradio.live` public link. If the network blocks these links, teams can demonstrate from the application shown within the notebook, and a mobile hotspot should be available for the demonstration laptop.

### On the day
- [ ] Prepare slides with: network details, links to notebooks and worksheets, step-by-step instructions (with screenshots) for creating a Groq API key, and how to find a mentor.
- [ ] Display or distribute the problem statements.
- [ ] Keep one or two spare Groq API keys **on mentor laptops only**, for teams unable to register. Do not show shared keys on slides or in group chats.

---

## 3. Guidance on problem selection

| Team profile | Recommended problem statement |
|---|---|
| No coding experience; prefers not to code | Problem 1 (Open Model Showdown) or Problem 2 (Build-a-Bot) |
| No coding experience; willing to try | Problem 3 (Persona Chatbot). Level 1 changes involve editing text only. |
| Interested in visual or interactive work | Problem 4 (Image Classifier). No API key is required. |
| Some Python experience | Problem 5 (Study Quiz Generator) |
| Has completed a programming course | Problem 6 (Document Question Answering) or Problem 7 (First-Issue Finder) |

Teams may switch to a simpler problem statement at the lunch break. A complete, working project is preferable to an incomplete, ambitious one.

---

## 4. Mentor reference

### Structure of the starter notebooks
- **Cell order:** installation → setup (reads the API key) → settings (team changes) → main function and quick test → application launch → optional extensions.
- **Demonstration mode:** if no `GROQ_API_KEY` secret is set, each notebook still runs and shows sample output. Teams can begin making changes before they have a key.
- **Error handling:** errors from the AI service are shown as a plain-language message starting with "Error:" and describing the corrective action. They do not stop the application.
- **Relaunching:** the launch cell calls `gr.close_all()` before `demo.launch(share=True)`, so re-running it replaces the previous application. A new public link is created each time.
- **Change markers:** comments marked **STUDENT TODO** are graded as Level 1 (text changes), Level 2 (settings) and Level 3 (new features). Direct teams that are stuck to the next Level 1 item.

### Common issues and resolutions

| Symptom | Cause | Resolution |
|---|---|---|
| `NameError: name 'X' is not defined` | Cells were skipped, run out of order, or the session restarted | Select **Runtime → Run all**, or run the cells in order. |
| Notebook remains in demonstration mode after a key is added | Incorrect secret name, or notebook access not enabled | The secret must be named exactly `GROQ_API_KEY`, with notebook access enabled. Re-run the setup cell. |
| "API key was rejected" | Incomplete copy, or key deleted | Create a new key at console.groq.com under API Keys. |
| "Usage limit reached" | Groq free-tier limits per minute or per day (per key) | Wait about one minute. Use `llama-3.1-8b-instant`, which has the highest limits. Reduce `MEMORY` (Problem 3) or `MAX_ISSUES` (Problem 7). Team members may each create a key. |
| Application does not reflect changes | The edited cell or the launch cell was not re-run | Re-run the edited cell and then the launch cell. |
| `SyntaxError` or `IndentationError` | Missing quotation mark, comma or bracket, or inconsistent indentation | Check the line shown in the error message and the line above it. |
| Problem 5: "response was not valid JSON" | The model occasionally produces incorrectly formatted output | Retry. If it happens repeatedly, lower `TEMPERATURE` and confirm the JSON section of the prompt is unchanged. |
| Problem 4: slow first run | The CLIP model (about 600 MB) is downloading | Expected; takes about one minute. A GPU runtime (Runtime → Change runtime type → T4 GPU) is optional. |
| Problem 6: "No text found" | The PDF contains scanned images only | Use a text-based PDF or the sample document provided. |
| Problem 7: GitHub rate limit | The unauthenticated limit (about 60 requests per hour) is shared by all users on the same network | Add a free fine-grained `GITHUB_TOKEN` secret, as described in the notebook. |
| Public link does not open | The venue network blocks gradio.live | Use the application shown within the notebook for the demonstration. |
| Colab session disconnected | Idle timeout or lost connection | Reconnect and select **Runtime → Run all**. Changes saved in the notebook are kept. |

### Recommended mentoring approach
- Ask the team what they want the application to do that it does not yet do, then direct them to the relevant STUDENT TODO item.
- Ask the team to read the last line of any error message, which usually identifies the problem.
- Encourage each team to complete the experiment described in its problem statement (for example, temperature comparison, accuracy measurement or chunk-size comparison). This turns the template into the team's own work and gives them substance for the presentation.

---

## 5. Judging

### Criteria (each scored from 1 to 5)

| Criterion | Description |
|---|---|
| Functionality | The demonstration works live. Additional credit for a public link or audience participation. |
| Originality | The concept goes beyond the template defaults, with at least one Level 2 or Level 3 change. |
| Understanding | The team can explain how the AI component works (for example system prompts, embeddings, structured output or zero-shot classification) and where it fails. |
| Evaluation | The team tested and measured its work, and reported failures as well as successes. |
| Presentation | Clear, well organised and within the time limit. |

### Suggested award categories
- Best Overall Project
- Best No-Code Project
- Best Persona Design
- Best Experiment or Evaluation
- Best Robustness Testing
- Open-Source Contribution Award (for example, a Problem 7 team that identified a real issue to work on)

---

## 6. After the event
- Share hacktoberfest.com and explain how to find issues labelled "good first issue".
- Encourage teams to publish their notebooks on GitHub with a README, as their first open-source repository.
- If the starter materials are hosted on GitHub, invite participants to submit pull requests that improve them (corrections, clearer instructions, new extensions) as a first Hacktoberfest contribution.
