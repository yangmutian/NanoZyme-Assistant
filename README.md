![图片1](https://github.com/user-attachments/assets/574387d9-a656-469f-92f7-7eadabbd7b86)

## 🧪 NanoZyme-Assistant

NanoZyme-Assistant (NZ-A) is an AI-driven framework for large-scale nanozyme discovery, integrating data construction, model prediction, and automated screening into a unified pipeline.

This project aims to accelerate nanozyme design by reducing reliance on manual trial-and-error and enabling efficient exploration of massive material spaces.

## 🚀 Overview

Nanozymes have emerged as promising candidates in catalysis, biomedicine, and environmental applications. However, discovering high-performance nanozymes remains challenging due to the vast search space.

NZ-A provides an end-to-end solution:

- 📊 Constructing large-scale nanozyme candidate databases  
- 🤖 Training AI models to predict catalytic activity  
- 🔍 Automatically screening high-potential materials  

## 🧠 Framework
NZ-A establishes an end-to-end screening pipeline for three representative nanozyme activities:

- **Peroxidase-like (POD)**
- **Oxidase-like (OXD)**
- **Catalase-like (CAT)**

Each activity is implemented as an independent module and corresponds to a dedicated folder in this repository, enabling flexible experimentation and extension.

## 📁 Project Components

To illustrate the project structure, we take the **Peroxidase-like (POD)** task as an example. The directory structure for POD is organized as follows:

### 1. 🧪 Code Pipeline

The complete workflow of NZ-A is implemented through a series of Jupyter notebooks:

- **Database Construction**
  - `1 download_pubmed.ipynb`  
    Build the nanozyme database using LLM-assisted literature mining.
  - `2 database_overview.ipynb`  
    Perform statistical analysis and visualization of the constructed database.

- **Data Preprocessing**
  - `3 process_peroxidase.ipynb`  
    Preprocess the nanozyme dataset (e.g., cleaning, filtering, feature preparation).
  - `4 process_materials_project.ipynb`  
    Preprocess data from the Materials Project database.
  - `5 process_data.ipynb`  
    Integrate the nanozyme database with Materials Project data to construct the final training dataset.

- **Model Training**
  - `6 model.ipynb`  
    Train the machine learning model for nanozyme activity prediction.
  - `7 model_year.ipynb`  
    Evaluate model performance (e.g., temporal generalization).

- **Large-scale Screening**
  - `8 predict_materials_project.ipynb`  
    Predict potential nanozymes from the Materials Project database.
  - `9 predict_aflow.ipynb`  
    Predict potential nanozymes from the AFLOW database.

### 2. 📊 Database

The constructed nanozyme database is publicly available:

- `./data/materials_project.xlsx`  

This dataset contains curated nanozyme-related information extracted and processed from literature and materials databases.

### 3. 🤖 Model

The trained models used for nanozyme discovery are provided:

- Stored in the `Model/` directory  
- Format: `.cbm` (CatBoost models)

These models can be directly used for inference and large-scale screening.
