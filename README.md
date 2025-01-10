# Qwen2-VL Document Classification Pipeline

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![Framework](https://img.shields.io/badge/Framework-HuggingFace-orange?logo=huggingface)
![Model](https://img.shields.io/badge/Model-Qwen2--VL-2B-lightgrey)
![License](https://img.shields.io/badge/License-MIT-green)
![Contributions](https://img.shields.io/badge/Contributions-Welcome-brightgreen?logo=github)
![GPU Required](https://img.shields.io/badge/Min%20GPU%20RAM-8GB-red)

---

Welcome to the **Qwen2-VL Document Classification Pipeline**! This project is a powerful, AI-driven solution designed to accurately classify documents into predefined categories. Using the **Qwen2-VL-2B-GPTQ-INT4 model**, this pipeline processes PDF and image files, applies natural language processing techniques, and generates insightful classification reports.

---

## **Table of Contents**
- [Features](#features)
- [Requirements](#requirements)
- [Setup](#setup)
- [Folder Structure](#folder-structure)
- [Supported Document Types](#supported-document-types)
- [Pipeline Workflow](#pipeline-workflow)
- [Results and Reporting](#results-and-reporting)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

---

## **Features**

- **End-to-End Document Processing**: Handles PDFs and images seamlessly.
- **Custom Prompt Engineering**: Incorporates domain-specific patterns for accurate classification.
- **Comprehensive Evaluation**: Generates confusion matrices and detailed classification reports.
- **Color-Coded Results**: Exports results to an Excel file for clear insights.
- **Multi-GPU Support**: Optimized for hardware acceleration.

---

## **Requirements**

### **Hardware Requirements**
- **Minimum CPU RAM**: 5 GB
- **Minimum GPU RAM**: 8 GB
- Additional memory for file storage and Docker layers.

### **Software Requirements**
- Python 3.10+
- Libraries: `torch`, `transformers`, `scikit-learn`, `pdf2image`, `pandas`, `matplotlib`, `seaborn`, `openpyxl`
- [Hugging Face Transformers](https://github.com/huggingface/transformers)

---

## **Setup**

### **1. Clone the Repository**
```bash
git clone <repository-url>
cd <repository-folder>
```

### **2. Install Dependencies**
```bash
apt-get update
apt-get install poppler-utils -y
pip install torch torchvision torchaudio scikit-learn pdf2image matplotlib seaborn openpyxl pandas
pip install git+https://github.com/huggingface/transformers
```

### **3. Download the Model**
The model is automatically downloaded during the pipeline execution or can be pre-downloaded using Hugging Face tools.

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


## **Pipeline Workflow**

1. **Load Model and Processor**
   - Leverages the Qwen2-VL-2B-GPTQ-INT4 model for classification.

2. **PDF Conversion and Image Merging**
   - Converts multi-page PDFs into vertically stacked images for efficient processing.

3. **Custom Prompt Engineering**
   - Builds prompts with domain-specific patterns and keywords for better predictions.

4. **Evaluation**
   - Generates a confusion matrix and classification report.
   - Saves results in a color-coded Excel file.

5. **Visualization**
   - Visualize classification performance using heatmaps and other plots.

---

## **Results and Reporting**

### **Outputs Generated**
- **Classification Accuracy**: Per-category and overall model performance metrics.
- **Confusion Matrix**: Heatmap visualization of expected vs predicted classifications.
- **Excel Reports**: Color-coded Excel files with classification details.

---

## **Future Enhancements**
- **OCR Integration**: Improve text extraction for better accuracy.
- **Model Fine-Tuning**: Incorporate additional labeled data.
- **Multilingual Support**: Expand capabilities to handle documents in multiple languages.
- **Advanced Models**: Explore LayoutLMv3 for complex layouts.

---

## **Contributing**
We welcome contributions! Here's how you can get involved:

1. Fork the repository.
2. Create a feature branch.
3. Submit a pull request with a detailed description of changes.

For major changes, please open an issue first to discuss your ideas.

---

## **License**
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

Thank you for exploring the **Qwen2-VL Document Classification Pipeline**. Happy coding! 🚀
