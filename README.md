# SlideCheck: PowerPoint and Image Text Analysis

This project extracts text from PowerPoint presentations and images, analyzes the extracted text for inconsistencies, and identifies potential contradictions and timeline mismatches.

## Overview

The script performs the following tasks:
1. Extracts text from each slide of a PowerPoint file.
2. Extracts text from images using Optical Character Recognition (OCR).
3. Analyzes the extracted text for:
   - Conflicting numerical data
   - Contradictory claims
   - Timeline mismatches based on dates

## Requirements

To run this project, you need:
- Python installed on your machine.
- The following Python libraries:
  - `python-pptx`
  - `Pillow`
  - `pytesseract`

### Installation

You can install the required libraries using pip. Open your terminal or command prompt and run:

```bash
pip install python-pptx Pillow pytesseract

```

## Tesseract OCR Installation
 
You also need to install Tesseract OCR, which is used for text extraction from images. Follow the instructions below based on your operating system:
- Windows: Download the installer from [Tesseract at UB Mannheim](https://github.com/UB-Mannheim/tesseract/wiki) and follow the installation instructions.
- macOS: Install via Homebrew by running:
  
```bash
brew install tesseract
```

- Linux: Install via your package manager. For example, on Ubuntu, run:

```bash
sudo apt-get install tesseract-ocr
```

Make sure to add Tesseract to your system's PATH.

## Usage
#### 1. Prepare Your Files: 
Place your PowerPoint file and any images you want to analyze in a directory.
#### 2. Edit the Script: 
Open the Python script and update the following variables to point to your files:
- 'pptx_file': Path to your PowerPoint file.
- 'image_files': List of paths to your image files.
#### 3. Run the Script: 
Execute the script using Python:
```bash
python SlideCheck.py
```

Replace SlideCheck.py with the actual name of your Python script.

## Functions
- #### extract_text_from_pptx(file_path): 
Extracts text from each slide in the PowerPoint presentation.
- #### extract_text_from_image(image_path): 
Extracts text from an image using Tesseract OCR.
- #### check_conflicting_numerical_data(text_data): 
Identifies conflicting numerical data across slides.
- #### check_contradictory_claims(text_data): 
Checks for contradictory claims within the text.
- #### check_timeline_mismatches(text_data): 
Identifies timeline mismatches based on dates found in the text.
- #### analyze_inconsistencies(text_data): 
Analyzes the text data for various inconsistencies.
- #### (pptx_file, image_files): 
Main function to extract text and analyze inconsistencies.

## Contributing
Contributions are welcome! If you have suggestions or improvements, feel free to submit a pull request or open an issue.
