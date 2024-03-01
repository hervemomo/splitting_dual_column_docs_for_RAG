# Separating Dual-Column PDF Documents for RAG Models

This repository contains a Jupyter notebook that outlines an approach for separating English and French texts from dual-column PDF documents. This preprocessing step is crucial for Retrieval-Augmented Generation (RAG) models, especially when dealing with documents that contain side-by-side bilingual content. RAG models, which leverage both retrieval mechanisms and generative capabilities, can significantly benefit from data that has been separated by language.

## Overview

The process involves reading a PDF file, iterating through each page, and extracting text from predefined regions corresponding to the two columns. Since the documents feature English and French texts in parallel columns, accurate text extraction is paramount. This entails identifying or estimating the coordinates of each column, which vary depending on the PDF's size and layout. For our purposes, we have divided each page vertically in half to delineate the columns, resulting in two rectangular areas (`fitz.Rect`) for text extraction.

## Prerequisites

Before running the notebook, ensure you have the following requirements installed:

- Python 3.x
- PyMuPDF (`fitz`)
- Any other libraries as specified in the notebook's requirements section

## Usage

1. Clone this repository to your local machine.
2. Install the required Python packages.
3. Open the `splitting_dual_column_docs_for_RAG.ipynb` notebook in Jupyter or a compatible environment.
4. Follow the instructions within the notebook to process your PDF files.

## Understanding the Coordinate System

Accurately extracting text from specific columns requires knowledge of the PDF's coordinate system. The coordinates for the text extraction areas are dependent on the document's layout. Generally, you may need to adjust the rectangle's coordinates based on your specific PDF. For more information on the coordinate system used by PyMuPDF, please visit:

[PyMuPDF Coordinates Documentation](https://pymupdf.readthedocs.io/en/latest/app3.html#coordinates)

## Purpose

The notebook demonstrates the essential process for separating English and French texts in dual-column PDFs, a step that optimizes the performance of Retrieval-Augmented Generation (RAG) models in processing legal documents and similar materials.

## Contributions

Contributions to this project are welcome. Please submit a pull request or open an issue if you have suggestions for improvement.
