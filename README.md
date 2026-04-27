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
