# MicroscopyLLM-Bench

# Microscopy Image Analysis and Classification

This repository provides a comprehensive pipeline for object detection, object classification, and image analysis on microscopic datasets. The workflows are implemented in Jupyter notebooks and focus on datasets of microscopic cell images and histopathological data.

## Project Overview
The repository includes:
1. Object detection and classification of cell images using machine learning models.
2. Analysis of PubMed histological datasets to generate descriptions and identify key features.
3. Detailed results and performance evaluation of multiple models.

## Directory Structure
```plaintext
.
|-- Datasets
|   |-- Brightfield Microscopy SCC
|   |-- Dreambooth Cell Images
|   |-- PubMedVision
|
|-- Notebooks
|   |-- Brightfield Microscopy SCC
|   |   |-- notebook_microscopic_dataset1_objdetection.ipynb
|   |-- Dreambooth Cell Images
|   |   |-- microscopic-object-classification-dataset2.ipynb
|   |-- PubMedVision
|       |-- pubmed-models.ipynb
|
|-- Results
|   |-- Brightfield Microscopy SCC
|   |   |-- gemini_1_Microscopic_ObjectDetection_results.json
|   |   |-- gemini_2_Microscopic_ObjectDetection_results.json
|   |   |-- intern_vl2_Microscopic_ObjectDetection_results.json
|   |-- Dreambooth Cell Images
|   |   |-- gemini_1_Datset2ObjClass_results.json
|   |   |-- gemini_2_Datset2ObjClass_results.json
|   |   |-- intern_vl2_Datset2ObjClass_results.json
|   |-- PubMedVision
|       |-- gemini_1_PubMED_results.json
|       |-- intern_vl2_PubMED_results.json
|       |-- llava_PubMED_results.json
|
|-- LICENSE
|-- README.md
```

## Datasets
The following datasets are used in this project:

1. **Dreambooth Cell Images**
   - [HuggingFace Dataset Link](https://huggingface.co/datasets/mario-dg/dreambooth-cell-images/viewer/default/train?p=45)
   - Contains microscopic cell images for object classification.

2. **PubMedVision**
   - [HuggingFace Dataset Link](https://huggingface.co/datasets/FreedomIntelligence/PubMedVision)
   - A dataset of histopathological and microscopic images for biomedical image analysis.

3. **Brightfield Microscopy SCC**
   - [HuggingFace Dataset Link](https://huggingface.co/datasets/mario-dg/brightfield-microscopy-scc)
   - Microscopy cell images for object detection tasks.

## Notebooks
The repository includes the following Jupyter notebooks:

### 1. Brightfield Microscopy SCC
**Notebook**: `notebook_microscopic_dataset1_objdetection.ipynb`
- Task: Object detection on microscopic images.
- Output: Detection results of elements like well edges and cell features.

### 2. Dreambooth Cell Images
**Notebook**: `microscopic-object-classification-dataset2.ipynb`
- Task: Object classification of microscopic cell images into categories:
  - Adherent cell
  - Cell with debris
  - Cell on well edge
- Output: Classified cell types and performance metrics.

### 3. PubMedVision
**Notebook**: `pubmed-models.ipynb`
- Task: Analysis of histopathological images from PubMedVision.
- Output: Automated descriptions of cellular structures, staining methods, and pathology insights.

## Results
Results are stored in JSON format for each notebook.

### Brightfield Microscopy SCC Results
- `gemini_1_Microscopic_ObjectDetection_results.json`
- `gemini_2_Microscopic_ObjectDetection_results.json`
- `intern_vl2_Microscopic_ObjectDetection_results.json`

### Dreambooth Cell Images Results
- `gemini_1_Datset2ObjClass_results.json`
- `gemini_2_Datset2ObjClass_results.json`
- `intern_vl2_Datset2ObjClass_results.json`

### PubMedVision Results
- `gemini_1_PubMED_results.json`
- `intern_vl2_PubMED_results.json`
- `llava_PubMED_results.json`

## How to Run
Follow these steps to run the notebooks:

1. Clone the repository:
   ```bash
   git clone <repo-url>
   cd <repo-name>
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

4. Open the notebooks from the `Notebooks` directory and run them cell-by-cell.

## Dependencies
The following libraries are required:
- Python 3.8+
- Jupyter Notebook
- HuggingFace Transformers
- PyTorch
- Pandas
- NumPy
- OpenCV

Install the required libraries using the provided `requirements.txt` file.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

## Acknowledgments
- [HuggingFace](https://huggingface.co/) for hosting datasets.
- All datasets contributors for their invaluable work.
