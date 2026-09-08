# OncoExtractAI-QA

OncoExtractAI-QA is a prototype project for extracting important lung cancer pathology information from clinical text reports.

The goal is not only to extract answers, but also to show the evidence sentence from the report that supports each answer. If the system cannot find a value or evidence, it marks the result as needing manual review.

## Project Goal

This project focuses on extracting four key oncology variables from lung cancer pathology reports:

- Histologic diagnosis
- Tumor size
- Pathologic T category, such as pT1 or pT2a
- Pathologic N category, such as pN0 or pN1

## Dataset

This project uses the TCGA-Reports pathology report dataset:

https://github.com/tatonetti-lab/tcga-path-reports

The full dataset is not included in this repository because it is large. Only sample outputs and project files are included.

## Current Prototype

The current notebook does the following:

1. Loads the TCGA-Reports CSV file.
2. Filters reports likely related to lung cancer.
3. Selects a 30-report sample.
4. Extracts histology, tumor size, pT, and pN using basic Python rules.
5. Finds evidence sentences for extracted values.
6. Assigns QA status as supported or manual review needed.
7. Saves the results as a CSV file.

## Files

- `notebooks/OncoExtractAI_QA.ipynb`: Main Google Colab notebook
- `lung_cancer_sample_reports.csv`: Sample reports used for the prototype
- `lung_cancer_label_template.csv`: Template for manual review labels
- `qa_extraction_results.csv`: Extracted results with evidence and QA status

## Tools Used

- Python
- Google Colab
- Pandas
- Regular expressions
- GitHub

## Project Status

This is an early prototype. The current version uses rule-based extraction. Future work may include improving evidence extraction, adding human-reviewed labels, calculating accuracy metrics, and building a simple review interface.
