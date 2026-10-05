# Problem Statement 4: Image Classifier

| | |
|---|---|
| **Level** | Beginner (modify lists and settings in working starter code) |
| **Team size** | 2–4 participants |
| **Starter code** | [templates/04_image_classifier.ipynb](../templates/04_image_classifier.ipynb) |
| **API key** | Not required |

---

## 1. Background

Teaching a computer to recognise objects in photos usually requires thousands of labelled example images.

**CLIP** is an open AI model that has learned to connect images with written descriptions. Because it understands text, it can sort a photo into any set of categories that are simply typed in, for example "samosa, dosa, pizza", without any extra training. This ability is called **zero-shot classification**.

## 2. Objective

Build a web application that identifies the contents of a photo, chosen from a **list of categories defined by the team**, and shows how confident the model is in its result.

A complete working example (a pet identifier) is provided. Teams replace it with their own theme.

## 3. Scope of Work

The completed application must:

1. Accept a photo by file upload or webcam.
2. Classify the photo into one of the team's chosen categories.
3. Show the confidence level for the top results (for example, "92% confident: dosa").
4. Show an "uncertain" message when confidence is below a set threshold.
5. Be reachable through a public web link.

Example themes: regional foods, recyclable and non-recyclable items, dog breeds, campus locations, facial expressions, plant types.

## 4. Key Terms

| Term | Meaning |
|---|---|
| Classifier | A program that assigns an input (such as an image) to one of several categories. |
| Label | The name of a category, such as "samosa". Labels are defined by the team. |
| CLIP | An open AI model that understands images and text together. |
| Zero-shot classification | Recognising categories the model was never specifically trained on. |
| Confidence | How certain the model is of its result, from 0% to 100%. |
| Accuracy | The proportion of correct results. For example, 8 correct out of 10 is 80% accuracy. |

## 5. Requirements

- A laptop with a web browser and a Google account
- The starter notebook, opened in Google Colab
- No API key or additional sign-up is required. The model runs within Google Colab at no cost.
- A mobile phone (optional) for testing with real objects

## 6. Approach

1. Open the notebook in Google Colab and run each cell in order (Shift + Enter). The first run downloads the model. The notebook then classifies a sample photo.
2. Select a theme and define the list of labels.
3. Make changes at the points marked **STUDENT TODO** in the code:
   - **Level 1:** application name, description, and list of labels
   - **Level 2:** label wording template and confidence threshold
   - **Level 3:** additional information per label, new features, or an alternative model
4. Run the "Launch the application" cell and test it with a webcam or phone camera.
5. Measure accuracy on 10 test photos, refine the labels, and measure again.

Clear, specific and visual labels generally perform better. For example, "golden retriever" performs better than "friendly dog".

## 7. Expected Deliverables

At the final demonstration, the team must present:

- [ ] A working application using the team's own theme and labels (not the provided example)
- [ ] A live demonstration using a webcam or phone photo
- [ ] Accuracy results on 10 test photos, before and after refining the labels
- [ ] A one-sentence explanation of zero-shot classification
- [ ] At least one example of an incorrect classification and a possible explanation for it


## 8. Optional Extensions

- Compare accuracy across the alternative models listed in the notebook.
- Find the conditions under which the model performs poorly (for example drawings, unusual angles, or several objects in one image).
- Build a practical use case, such as sorting waste into recycling, compost, and general waste.
- Add a selection menu to switch between several label sets.
