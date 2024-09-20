
# Amazon ML Hackathon: OCR and Entity Extraction from Images

## Project Overview

This project, developed for Amazon's annual machine learning hackathon, focuses on extracting specific entity information from product images using Optical Character Recognition (OCR) and regex-based entity extraction.

## Key Features

- Processes images from a dataset
- Extracts text using OCR (easyocr library)
- Identifies entities like dimensions, weight, and volume
- Standardizes units of measurement

## Technical Requirements

- Python 3.x
- Libraries: pandas, easyocr, requests, Pillow, re

## Implementation Guide

1. **Data Preparation**: Create a CSV file with columns for image links, entity names, and group IDs.
2. **Script Configuration**: Set the `csv_file_path` variable to your CSV file location.
3. **Execution**: Run the script to process images and extract entities.
4. **Results**: View output in `processed_results.csv`.

## Script Components

1. **Data Loading**: Imports image URLs and entity specifications from CSV.
2. **OCR Setup**: Initializes English text recognition.
3. **Entity Extraction**: Uses regex to identify and standardize measurement units.
4. **Unit Conversion**: Maps abbreviations to full unit names.
5. **Main Processing Loop**:
   - Retrieves images from URLs
   - Applies OCR
   - Extracts and formats entity information
   - Compiles results into a dataframe

## Output Format

The resulting CSV includes:
- `image_url`: Source of the processed image
- `entity_value`: Extracted information as "<numeric value> <unit>"