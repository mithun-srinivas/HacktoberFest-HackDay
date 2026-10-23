# Hacktoberfest Hack Day: Open-Source AI

Welcome to the Hacktoberfest Hack Day. The theme is **open-source AI and open-weight models**. All tools and models used are free. The coding themes run in **Google Colab**, so nothing needs to be installed.

## Choose a theme

See **[PROBLEM_STATEMENTS.md](PROBLEM_STATEMENTS.md)** for full details. Each team of 4–6 participants selects one theme.

| No. | Theme | Level | Starter material |
|---|---|---|---|
| 1 | [Open Model Evaluation](problem-statements/01_model_evaluation.md) | Beginner (no coding) | [Worksheet](worksheets/01_model_evaluation.md) |
| 2 | [RAG Application with Gemma](problem-statements/02_rag_application.md) | Intermediate | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/02_rag_starter_kit.ipynb) |
| 3 | [Fine-Tuning Gemma](problem-statements/03_fine_tuning.md) | Advanced | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/03_fine_tuning_starter_kit.ipynb) |

## Getting started

**Theme 1 (no coding):** open the worksheet and follow the steps. You will need a Google account and a free GroqCloud account (console.groq.com).

**Themes 2 and 3 (Google Colab):**
1. Select **Open in Colab** for your theme in the table above, and sign in with a Google account.
2. Select **File → Save a copy in Drive** so that your changes are saved.
3. Set up the runtime for your theme:
   - **Theme 2:** no GPU is needed. Create a free API key at **aistudio.google.com/apikey** and add it in the Colab **Secrets** panel (key icon, left sidebar) under the name `GOOGLE_API_KEY`, with Notebook access enabled.
   - **Theme 3:** select **Runtime → Change runtime type → T4 GPU → Save**. No API key is needed; Gemma 4 runs inside the notebook.
4. Run the cells in order from top to bottom (**Shift + Enter**). The first run installs the required libraries and downloads the models, which takes a few minutes.
5. Make your changes at the points marked **STUDENT TODO**.
