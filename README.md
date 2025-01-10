# Qwen2-VL Document Classification Pipeline

Welcome to the **Qwen2-VL Document Classification Pipeline** project! This repository contains a Python-based implementation for classifying various document types using the Qwen2-VL-2B-GPTQ-INT4 model. The project processes PDF and image files, applies natural language processing techniques, and generates classification reports.

---

## **Project Overview**
This pipeline is designed to classify documents into predefined categories using the Qwen2-VL model. The main features include:
- Converting multi-page PDFs to vertically merged images for processing.
- Building a robust prompt with domain-specific patterns and keywords.
- Generating confusion matrices, classification reports, and exporting results to an Excel file.

---

## **Table of Contents**
- [Requirements](#requirements)
- [Setup](#setup)
- [Folder Structure](#folder-structure)
- [Supported Document Types](#supported-document-types)
- [Pipeline Steps](#pipeline-steps)
- [Results and Reporting](#results-and-reporting)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

---

## **Requirements**

**Hardware Requirements:**
- **Minimum CPU RAM:** 5 GB
- **Minimum GPU RAM:** 8 GB
- Additional memory for file storage and Docker layers.

**Software Requirements:**
- Python 3.10+
- Libraries: `torch`, `transformers`, `scikit-learn`, `pdf2image`, `pandas`, `matplotlib`, `seaborn`, `openpyxl`
- [Hugging Face Transformers](https://github.com/huggingface/transformers)

---

## **Setup**

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Install Dependencies**
   ```bash
   apt-get update
   apt-get install poppler-utils -y
   pip install torch torchvision torchaudio scikit-learn pdf2image matplotlib seaborn openpyxl pandas
   pip install git+https://github.com/huggingface/transformers
   ```

3. **Download the Model**
   The model can be downloaded automatically during the pipeline's execution or pre-downloaded using Hugging Face tools.

---

## **Folder Structure**
Ensure your file structure follows the format below for proper pipeline execution:
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
   The pipeline uses the Qwen2-VL-2B-GPTQ-INT4 model for classification.

2. **PDF Conversion and Image Merging**
   Multi-page PDFs are converted to vertically stacked images for better processing.

3. **Prompt Engineering**
   Domain-specific patterns and keywords are utilized to generate accurate predictions.

4. **Evaluation**
   - Generates confusion matrices and classification reports.
   - Saves results in a color-coded Excel file.

5. **Visualization**
   - Visualize classification performance using heatmaps and other plots.

---

## **Results and Reporting**
Results include:
- **Classification Accuracy:** Per-category accuracy and overall model performance.
- **Confusion Matrix:** Heatmap of expected vs predicted classifications.
- **Excel Reports:** Color-coded Excel files with classification results.

---

## **Future Enhancements**
- Integration of OCR to improve text extraction.
- Fine-tuning using additional labeled data.
- Support for multilingual documents.
- Addition of discriminative models like LayoutLMv3 for complex layouts.

---

## **Contributing**
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a feature branch.
3. Submit a pull request with a detailed description of changes.

---

## **License**
This project is licensed under the MIT License. See the `LICENSE` file for details.
