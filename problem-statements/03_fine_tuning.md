# Theme 3: Fine-Tuning Gemma

| | |
|---|---|
| **Level** | Advanced |
| **Team size** | 4–6 participants |
| **Platform** | Google Colab (free T4 GPU), Unsloth |
| **Starter kit** | [Open in Colab](https://colab.research.google.com/github/mithun-srinivas/HacktoberFest-HackDay/blob/main/templates/03_fine_tuning_starter_kit.ipynb) |

---

## 1. Background

A general-purpose model can be adapted to a specific task by **fine-tuning**: continuing its training on examples of that task. Fine-tuning is useful when a task needs a consistent format, specialised terminology or behaviour that prompting alone does not reliably produce.

**LoRA (Low-Rank Adaptation)** makes fine-tuning practical on limited hardware. It leaves the original model weights unchanged and trains a small set of additional weights. With **Unsloth**, Google's open-weight **Gemma 4** model can be fine-tuned on a free Colab GPU.

A fine-tuned model is only useful if it is measurably better than the original. Every fine-tuning project therefore needs a fair comparison against the plain model.

## 2. Objective

Fine-tune Gemma 4 for one of the two problem statements below, build an application around the fine-tuned model, and present a **comparative analysis** of the plain and fine-tuned models.

## 3. What is Provided

The starter kit is a complete, working Colab notebook that demonstrates the full workflow on a sample task (IT support ticket triage):

- Loading the plain **Gemma 4 E2B** model with Unsloth
- A training set and a separate test set
- A **baseline evaluation** of the plain model with automatic scoring
- **LoRA fine-tuning** on a free T4 GPU
- Evaluation of the fine-tuned model and a **comparison table**
- A Gradio application that shows the plain and fine-tuned models side by side
- Saving the fine-tuned adapters
- Guidance and example code for loading the datasets below and for fine-tuning on images (Problem 3B)

## 4. Problem Statements (choose one)

### 3A. Teach Gemma to Understand Code-Mixed Regional Languages

**Problem statement:** People frequently mix English with regional languages when chatting, but AI models may struggle with informal expressions, transliteration and mixed scripts. Fine-tune Gemma to understand and generate natural code-mixed text in **Kannada or Hindi** (choose one).

**Dataset:** AI4Bharat IndicCMix, `ai4bharat/IndicCMix` on Hugging Face (https://huggingface.co/datasets/ai4bharat/IndicCMix). Use the file for your chosen language: `ka.parquet` (Kannada) or `hi.parquet` (Hindi). Each example has the same sentence in four forms: `english`, `native_script_codemixed`, `full_native_script` and `romanized_casual`.

**Access:** the dataset is gated. Each team needs a free Hugging Face account, must accept the dataset's terms on its page, and must add a Hugging Face access token to Colab Secrets as `HF_TOKEN` (instructions are in the starter kit). The dataset is small, so check the number of examples in your chosen language file when planning the training and test sets.

**Expected output:** a model that converts between English, regional-script text and informal romanized language, evaluated on a held-out test set with an automatic measure (for example the chrF score) and a human rating of naturalness by a speaker of the language.

### 3B. Extract Information from Receipts

**Problem statement:** People and businesses enter information from receipts into expense trackers by hand. Fine-tune a Gemma model that supports images to extract the merchant, date, address and total from receipt images.

**Dataset:** ICDAR 2019 SROIE, `jsdnrs/ICDAR2019-SROIE` on Hugging Face (https://huggingface.co/datasets/jsdnrs/ICDAR2019-SROIE; CC BY 4.0). It contains 626 training and 361 test receipt images, each annotated with `company`, `date`, `address` and `total`.

**Model:** Gemma 4 E2B supports images. Fine-tuning on images uses Unsloth's `FastVisionModel` instead of the text-only workflow in the starter kit. The starter kit includes the required changes, based on Unsloth's official Gemma 4 vision notebook.

**Expected output:** structured receipt data (JSON with the four fields), with field-level extraction accuracy measured on the test set for the plain and fine-tuned models.

### For either problem statement, the team will:

1. **Baseline:** test the plain Gemma model on the use case and record how it performs.
2. **Data:** prepare a training set and a separate test set for the use case.
3. **Fine-tune:** train LoRA adapters on the training set, recording the settings used.
4. **Compare:** evaluate the plain and fine-tuned models on the same test set with the same scoring method.
5. **Build:** create an application around the fine-tuned model for the intended users.

## 5. Key Terms

| Term | Meaning |
|---|---|
| Fine-tuning | Continuing a model's training on examples of a specific task. |
| LoRA | Low-Rank Adaptation: training a small set of additional weights instead of the whole model. |
| Base / plain model | The original model before fine-tuning. |
| Training set | The examples the model learns from. |
| Test set | Separate examples used only to measure performance. They must never be used for training. |
| Overfitting | When a model memorises the training examples instead of learning the task, and performs poorly on new examples. |
| Baseline | The performance of the plain model, used as the point of comparison. |
| Unsloth | An open-source library for fast, memory-efficient fine-tuning. |

## 6. Requirements

- A laptop with a web browser and a Google account
- The starter kit, opened in Google Colab with a **T4 GPU** runtime
- For Problem 3A: a free Hugging Face account, with the IndicCMix terms accepted and an access token (huggingface.co/settings/tokens)

Colab limits free GPU time per account. Plan training runs carefully, and use team members' accounts for parallel experiments.

## 7. Expected Deliverables

At the showcase, the team must present:

- [ ] A **fine-tuned model** for the use case, with the training settings documented
- [ ] A **dataset description:** source, size, format, and how the training and test sets were separated
- [ ] A **comparative analysis** of the plain and fine-tuned models on the same test set, with metrics and example outputs
- [ ] A **working application** built around the fine-tuned model, demonstrated live
- [ ] A **discussion** of where fine-tuning helped, where it did not, and why

## 8. Good to Have (bonus points)

- **Prompted baseline:** also compare with the plain model given a detailed, well-engineered prompt, to show what fine-tuning adds beyond prompting.
- **Training experiments:** compare dataset sizes, training steps, LoRA rank or learning rate, and present the effect.
- **Overfitting check:** measure performance on examples that differ clearly from the training data.
- **Model size comparison:** fine-tune Gemma 4 E4B as well, and compare quality, speed and memory use.
- **Combined approach:** combine the fine-tuned model with retrieval (RAG).
- **Publishing:** share the adapters on Hugging Face with a model card describing the training data, intended use and limitations.
- **Error analysis:** categorise the fine-tuned model's remaining errors and propose improvements.
- **3A only:** support both Kannada and Hindi in one model, or handle mixed-script input such as chat messages.
- **3B only:** extract the individual line items (item, quantity, price) as well as the four required fields.
