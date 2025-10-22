# Streamlit Tesseract & EasyOCR OCR App 📝

Streamlit application to extract text from images and PDFs using **Tesseract OCR** for printed text and **EasyOCR** for handwritten text.

---

## Streamlit Demo

![App Screenshot](project_demo/streamlit%20demo.png)


## Project Structure

```
STREAMLIT-TE...
│
├─ .streamlit/
├─ .vscode/
├─ data/
├─ helpers/
│ ├─ constants.py
│ ├─ easy_ocr.py
│ ├─ opencv.py
│ ├─ pdfimage.py
│ ├─ style.css
│ └─ tesseract.py
├─ .gitignore
├─ README.md
├─ requirements.txt
├─ streamlit_app.old.py
└─ streamlit_app.py
```

- **helpers/constants.py** – Stores global constants, language options, flags, and default indexes.  
- **helpers/easy_ocr.py** – Contains EasyOCR helper functions for handwritten OCR.  
- **helpers/opencv.py** – Image preprocessing functions (grayscale, denoising, thresholding, rotation).  
- **helpers/pdfimage.py** – Convert PDF pages to images.  
- **helpers/tesseract.py** – Tesseract OCR helper functions.  
- **helpers/style.css** – Custom CSS for Streamlit UI.  
- **streamlit_app.py** – Main Streamlit app.  
- **streamlit_app.old.py** – Backup/old version of the app.  
- **requirements.txt** – Python dependencies.

---

## Features

- Upload images or PDFs (png, jpg, jpeg, bmp, tif, tiff, pdf)  
- Preprocess images before OCR:
  - Grayscale conversion  
  - Denoising  
  - Thresholding  
  - Rotation (90° or free angle)  
- Select OCR type: Printed (Tesseract) or Handwritten (EasyOCR)  
- Preview processed images and extracted text  
- Download extracted text as `.txt` file  
- Multiple languages supported for Tesseract OCR

---

## Installation

1. Clone the repository:

```
git clone <your-repo-url>
cd STREAMLIT-TE...
```
## Install Dependencies

```
pip install -r requirements.txt
```

## Install Tesseract OCR:

Windows: Tesseract installer from UB Mannheim

macOS: brew install tesseract

Linux: sudo apt install tesseract-ocr

## Run The App
```
streamlit run streamlit_app.py
