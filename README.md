# Qwen2-VL Document Classification Pipeline

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white) ![Framework](https://img.shields.io/badge/Framework-HuggingFace-orange?logo=huggingface) ![Model](https://img.shields.io/badge/Model-Qwen2--VL-2B-lightgrey?logo=openai) ![License](https://img.shields.io/badge/License-MIT-green) ![Contributions](https://img.shields.io/badge/Contributions-Welcome-brightgreen?logo=github) ![GPU Required](https://img.shields.io/badge/Min%20GPU%20RAM-8GB-red)

Welcome to the **Qwen2-VL Document Classification Pipeline** project! This repository showcases a powerful, streamlined pipeline for classifying various document types using the **Qwen2-VL-2B-GPTQ-INT4** model.

---

## **Project Overview**
This pipeline leverages cutting-edge AI technology to classify documents into predefined categories. It supports image and PDF input formats, processes documents with efficient natural language understanding, and outputs precise classification reports and confusion matrices.

**Key Features:**
- Multi-page PDF handling with vertical merging of pages for seamless processing.
- Optimized prompt engineering for domain-specific accuracy.
- Automatic evaluation with detailed reports and visualizations.
- Simple execution in Google Colab — no additional setup required!

---

## **Table of Contents**
- [Requirements](#requirements)
- [Setup](#setup)
- [Usage in Google Colab](#usage-in-google-colab)
- [Folder Structure](#folder-structure)
- [Pipeline Steps](#pipeline-steps)
- [Results and Reporting](#results-and-reporting)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)

---

## **Requirements**

**Hardware Requirements:**
- **Minimum CPU RAM:** 5 GB
- **Minimum GPU RAM:** 8 GB
- Additional memory for file storage.

---

## **Setup**
No complex installations or dependencies! Open the notebook in Google Colab, upload your files, and run the cells sequentially.

---

## **Usage in Google Colab**

1. **Open the Notebook**
   Open the project notebook in Google Colab using this [link](https://colab.research.google.com/).

2. **Upload Your Files**
   Place your documents in the appropriate folders and mount your Google Drive.

3. **Run the Notebook**
   Execute the cells sequentially to:
   - Load the model and processor.
   - Convert PDFs to images.
   - Classify documents and generate reports.

4. **Download Results**
   Results (Excel file, confusion matrix) are saved in the outputs directory for easy access.

---

## **Folder Structure**

Ensure your file structure follows this format for proper pipeline execution:
```
root_directory/
    ├── azure_files/
    │   ├── bill_of_lading/
    │   ├── customs_document/
    │   ├── delivery_receipt/
    │   ├── invoice/
    │   ├── ... (other categories)
    └── outputs/
        ├── classification_results.xlsx
        ├── confusion_matrix.png
```

---


## **Pipeline Steps**

1. **Load Model and Processor**
   The pipeline utilizes the Qwen2-VL-2B-GPTQ-INT4 model for document classification.

2. **PDF Conversion and Image Merging**
   Multi-page PDFs are converted to vertically stacked images to ensure seamless input to the model.

3. **Prompt Engineering**
   Employs domain-specific patterns and keywords for improved classification accuracy.

4. **Evaluation**
   - Generates detailed confusion matrices and classification reports.
   - Produces color-coded Excel files for results.

5. **Visualization**
   Heatmaps and graphical representations provide insights into model performance.

---

## **Results and Reporting**

**Outputs Include:**
- **Classification Accuracy:** Per-category and overall performance.
- **Confusion Matrix:** Heatmap of expected vs predicted classifications.
- **Excel Reports:** Color-coded Excel files summarizing results.

---

## **Future Enhancements**
- Integration with OCR for enhanced text extraction.
- Support for multilingual document classification.
- Fine-tuning with additional labeled datasets.
- Adoption of advanced models like LayoutLMv3 for complex layouts.

---

## **Contributing**
We welcome contributions from the community! To contribute:
1. Fork the repository.
2. Create a feature branch.
3. Submit a pull request with a detailed explanation of your changes.

---


**Start Classifying with Ease!** 🚀
