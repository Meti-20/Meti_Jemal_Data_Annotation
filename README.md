# Meti Jemal - AI Data Annotation & Labeling Portfolio

Welcome to my AI Data Annotation portfolio. This repository contains structured production-ready datasets, custom labeling interface schemas, and pipeline documentation built using industry-standard tools like **Label Studio**. 

This portfolio demonstrates my technical competency in formatting data schemas, handling data validation structures, and annotating data for both **Natural Language Processing (NLP)** and **Computer Vision (CV)**.

---

## 📁 Repository Structure
```text
├── NLP-Text-Annotation/
│   ├── NER_News_Data.json              # Exported annotated Named Entity Recognition dataset
│   ├── Sentiment_Reviews_Data.csv      # Exported annotated Sentiment analysis dataset
│   ├── Customer_Intents_Data.json      # Exported annotated Chatbot intent dataset
│   └── label_studio_configs/           # Custom XML interface layouts
├── Computer-Vision-Annotation/         # Workspace allocated for CV/Image assets
│   └── Image_Bounding_Boxes.json       # Bounding box and segmentation metadata outputs
└── README.md                           # Portfolio documentation
```

---

## 🛠️ Section 1: Text Annotation for NLP (Module 4)

This section highlights datasets engineered for localized contexts, handling linguistic challenges like code-switching, expressions, and regional entities.

### Track 1: Named Entity Recognition (NER)
* **Objective:** Extract and categorize key entities within regional news data into predefined target tokens.
* **Target Tags:** `PER` (Person), `LOC` (Location), `ORG` (Organization).
* **Interface XML Schema:**
```xml
<View>
  <Labels name="label" toName="text">
    <Label value="PER" background="#3498DB" hint="Person"/>
    <Label value="LOC" background="#2ECC71" hint="Location"/>
    <Label value="ORG" background="#E67E22" hint="Organization"/>
  </Labels>
  <Text name="text" value="$text"/>
</View>
```

### Track 2: Customer Sentiment Analysis
* **Objective:** Audit consumer review datasets and determine the overall tone polarity.
* **Target Tags:** `Positive`, `Neutral`, `Negative`.
* **Key Challenge Solved:** Audited mixed-sentiment strings (e.g., *"The food was great, but the music was too loud"*) to balanced `Neutral` metrics based on multi-element cancelation logic.

### Track 3: Intent Classification for Chatbots
* **Objective:** Map transactional customer dialogs into actionable operational labels for financial chat systems.
* **Target Tags:** `Inquiry` (Balance/Status inquiries), `Complaint` (Error messages/App crashes), `Feedback` (Suggestions).
* **Data Engineering Fix:** Handled validation parsing errors by adjusting target value strings to dynamically access deep nested JSON objects (`$humanMachineDialogue.text`).

---

## 📸 Section 2: Computer Vision Annotation

* **Objective:** Object detection, classification, and spatial labeling for computer vision architectures.
* **Tasks Executed:** Spatial bounding boxes, dataset scaling, and class distribution verification.
* **Output Format:** Image annotation coordinates and structural spatial values are exported and saved within the `/Computer-Vision-Annotation/` directory.

---

## 📈 Quality Assurance & Validation Standards
To ensure high-quality dataset curation for production models, my workflow follows strict annotation guidelines:
1. **Consistency:** Maintaining zero tag-drift across extended sets of data tasks.
2. **Schema Resolution:** Debugging JSON validation mismatches to preserve nested data parameters.
3. **Contextual Awareness:** Integrating linguistic markers and local expressions to keep classification clean.

---
**Contact:** Connect with me on [LinkedIn](https://linkedin.com) to discuss data pipelines, model optimization, and AI annotation engineering projects!
