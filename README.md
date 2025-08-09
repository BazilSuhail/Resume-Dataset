# Resume-Dataset

## Overview
**Resume-Dataset** is a Python-based project to generate PDF CVs from a LaTeX template and a CSV dataset, designed for creating a structured dataset for training LayoutLM, a model for document understanding. The repository includes a LaTeX template (`cv_template.tex`) and a sample CSV dataset (`cv_data.csv`) to generate CVs, which can be processed for text and layout extraction.

## Repository Contents
- `cv_template.tex`: Injectable LaTeX template with placeholders for CV data.
- `cv_data.csv`: Sample dataset with resume data for two individuals (Sourabh Bajaj, Jane Smith).

## Approach
- Parse CSV data containing resume details (name, email, mobile, website, education, experience, projects, languages, technologies).
- Inject CSV data into LaTeX template placeholders.
- Compile LaTeX files to PDFs using `pdflatex`.
- Clean up auxiliary files (`.aux`, `.log`, `.tex`) after compilation.
- Enable dataset creation for LayoutLM by providing PDFs for text and bounding box extraction.

## Usage
1. Install dependencies: `texlive`, `pandas`.
2. Place `cv_template.tex` and `cv_data.csv` in the working directory.
3. Run `generate_cvs.py` to produce PDFs (e.g., `CV_Sourabh_Bajaj.pdf`, `CV_Jane_Smith.pdf`).
4. Use PDFs for LayoutLM dataset preparation (e.g., extract text and bounding boxes with `pdfplumber`).

## Prerequisites
- Python 3.6+
- LaTeX distribution (TeX Live/MiKTeX)
- `pandas` library

## Installation (Google Colab)
```python
!apt-get update
!apt-get install -y texlive texlive-latex-extra texlive-fonts-extra
!pip install pandas
```