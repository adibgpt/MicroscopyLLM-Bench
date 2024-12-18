# MicroscopyLLM-Bench

This repository provides a comprehensive pipeline for object detection, object classification, and image analysis on microscopic datasets. The workflows are implemented in Jupyter notebooks and focus on datasets of microscopic cell images and histopathological data.

## Project Overview
The repository includes:
1. Object detection and classification of cell images using machine learning models.
2. Analysis of PubMed histological datasets to generate descriptions and identify key features.
3. Detailed results and performance evaluation of multiple models.

![image](https://github.com/adibgpt/MicroscopyLLM-Bench/blob/7abb0436e47142aabbee7e0d07bd7fe90ce9fdfb/workflow.png)

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

![image](https://github.com/adibgpt/MicroscopyLLM-Bench/blob/5f5eaea5cb3eb68eeb329e47051da9d9fbab2ff3/Datasets/Dreambooth%20Cell%20Images/image%20(9).jpg)

2. **PubMedVision**
   - [HuggingFace Dataset Link](https://huggingface.co/datasets/FreedomIntelligence/PubMedVision)
   - A dataset of histopathological and microscopic images for biomedical image analysis.

![image](https://github.com/adibgpt/MicroscopyLLM-Bench/blob/815cdb365b72afa7a1365135c10aea509ff785ed/Datasets/PubMedVision/pmc_13_0.jpg)

3. **Brightfield Microscopy SCC**
   - [HuggingFace Dataset Link](https://huggingface.co/datasets/mario-dg/brightfield-microscopy-scc)
   - Microscopy cell images for object detection tasks.

![image](https://github.com/adibgpt/MicroscopyLLM-Bench/blob/9cc09d55270038145a6c83b67a49a50847a2353e/Datasets/Brightfield%20Microscopy%20SCC/image%20(2).png)

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

![image](https://github.com/adibgpt/MicroscopyLLM-Bench/blob/66e4cce95e35ba5056f116a03f644a877e6b43e0/Brightfield%20Microscopy%20SCC-gemini1.5flash.png)
![image](https://github.com/adibgpt/MicroscopyLLM-Bench/blob/b3e87082f69d1683deec8c1d3186a5ef132980bf/Brightfield%20Microscopy%20SCC-gemini1.5pro.png)

### Dreambooth Cell Images Results
- `gemini_1_Datset2ObjClass_results.json`
- `gemini_2_Datset2ObjClass_results.json`
- `intern_vl2_Datset2ObjClass_results.json`

![image](https://github.com/adibgpt/MicroscopyLLM-Bench/blob/1f17103e5dc154f009c26ff78f6fb6904ef9123a/Dreambooth%20Cell%20Images-gemini1.5flash.png)

### PubMedVision Results
- `gemini_1_PubMED_results.json`
- `intern_vl2_PubMED_results.json`
- `llava_PubMED_results.json`

## How to Run
Follow these steps to run the notebooks:

1. Clone the repository:
   ```bash
   git clone https://github.com/adibgpt/MicroscopyLLM-Bench.git
   cd MicroscopyLLM-Bench
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
