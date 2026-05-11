Author: Anderia Nisar

Course: Introduction to Applied Artificial Intelligence

Instructor: Dr. Faiz Ahmad

OCR Basics: Receipt Text Extraction

This repository contains a Python-based implementation for extracting text from receipt images using Tesseract OCR and EasyOCR. The project focuses on image preprocessing techniques and a comparative analysis of different OCR engines to evaluate their effectiveness on retail documents.

Project Structure

week5-ocr-basics.ipynb: The main Jupyter Notebook containing the implementation, image processing steps, and results.Data: Utilizes a dataset of receipt images for training and testing OCR accuracy.

Key Features

Dual OCR Engine Support:
Implementation of both pytesseract and easyocr.
Advanced Preprocessing:
Uses OpenCV for grayscale conversion and Otsu’s Thresholding to improve character recognition.
Structured Data Analysis:
Extracts key fields such as Merchant Name, Time, and Receipt Number.
Performance Comparison:
Analyzes how different models handle noisy backgrounds and stylized fonts.
Getting Started

Prerequisites
Ensure you have the following 
installed:
Python 3.xTesseract OCR EngineInstallationClone the repository and install the required Python libraries:Bashgit clone https://github.com/your-username/OCR-Receipt-Text-Extraction.git
cd OCR-Receipt-Text-Extraction
pip install pytesseract easyocr opencv-python Pillow matplotlib

WorkflowImage Loading: 

Receipts are loaded from the dataset directory.Preprocessing:Grayscale: Converts images to 8-bit for simplified processing.

Thresholding:

Binarizes the image using cv2.THRESH_OTSU to isolate text from the background.Extraction: Tesseract and EasyOCR process the images to generate raw string data.

Evaluation:

Results are tabulated to compare accuracy across different receipt layouts.

Observations:
Tesseract is highly efficient for standard, high-contrast fonts.EasyOCR demonstrates better robustness against irregular fonts and slight rotations.Future EnhancementsImplementing denoising filters (Gaussian/Median blur) for low-quality scans.Adding automated field parsing using Regular Expressions (Regex).
Intelligent Document Processing


A FastAPI-based OCR and document extraction API that classifies documents and extracts dates, amounts, and entities from scanned receipts or other images.

Features


OCR using Tesseract
Document classification using pre-trained joblib model files
Date, amount, and entity extraction using regex and spaCy
FastAPI endpoints for classification, extraction, and combined processing
Requirements
Python 3.12+
Tesseract OCR installed on Windows
Python packages listed in requirements.txt
Setup


Create and activate a virtual environment:
python -m venv venv
.\venv\Scripts\Activate.ps1
Install Python dependencies:
pip install -r requirements.txt

Install Tesseract OCR for Windows:


Download from https://github.com/UB-Mannheim/tesseract/wiki
Install and make sure tesseract.exe is on your PATH
Running the API
cd C:\Users\PMLS\Downloads\Intelligent_Document_Processing
uvicorn main:app --reload

Then open the API docs at:

http://127.0.0.1:8000/docs

Project structure


main.py - FastAPI application
extractors.py - extraction helper functions
requirements.txt - Python dependencies
.gitignore - ignored files for git


Notes

If Tesseract is not on the system PATH, main.py is configured to use C:\Program Files\Tesseract-OCR\tesseract.exe.
The model files vectorizer.pkl and classifier.pkl must be present in the project folder.
