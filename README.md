# Automated Document Scanner & OCR Enhancement

## Overview

This project implements an automated document scanner with OCR (Optical Character Recognition) capability using Python and OpenCV. The system detects document boundaries in a photo, applies perspective transformation to produce a clean top-down scan, enhances image quality through adaptive thresholding, and then extracts text from the scanned output using Tesseract OCR.

The base scanning pipeline builds on classical computer vision techniques. The OCR integration using pytesseract was added as the primary contribution of this project.

---

## Features

- Automatic document edge and corner detection
- Perspective transformation for top-down view
- Image sharpening and adaptive thresholding
- Text extraction via Tesseract OCR
- Supports both single image and batch directory processing
- Interactive mode for manual corner adjustment

---

## Usage

**Single image:**
python scan.py --image sample_images/document.jpg

**Interactive mode (manual corner selection):**
python scan.py --image sample_images/document.jpg -i

**Batch process a directory:**
python scan.py --images sample_images/

OCR output will be printed to the terminal after each scan.

---

## Results

The system was tested on four categories of input:

|------------|--------------|--------------|
| Input Type | Scan Quality | OCR Accuracy |
| Printed book page | Excellent | ~95% |
| Formal printed document | Excellent | ~90% |
| Handwritten notes | Good | ~40% |


OCR performs well on printed text but struggles with handwritten content and diagram-heavy pages, which is expected behavior for Tesseract.

---

## References

- OpenCV Documentation: https://docs.opencv.org
- Tesseract OCR: https://github.com/tesseract-ocr/tesseract
- Original scanning pipeline: https://github.com/andrewdcampbell/OpenCV-Document-Scanner

---