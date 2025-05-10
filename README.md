# csv2bib
This code will convert Scopus csv file to bib format. 
# CSV to BibTeX Converter (csv2bib)

`csv2bib.py` is a Python script designed to convert bibliographic data from CSV (Comma Separated Values) files from scopus into BibTeX format.

## Aim

The primary goal of this script is to simplify the management and conversion of bibliographic references. Many researchers and academics find it easier to collect and edit publication data in a spreadsheet program (saving as CSV). This script allows you to:

1.  **Easily edit your bibliographic data** in a familiar CSV format.
2.  **Convert this data into BibTeX (`.bib`) files**, which are widely used by citation management software (like Zotero, Mendeley, EndNote).
3.  **Prepare data for bibliometric analysis tools** like [biblioemtrix](https://www.bibliometrix.org/) in R, which often require BibTeX files as input.

This is particularly useful when dealing with data exported from Scopus, allowing for manual cleaning and augmentation before further processing.

## Features

*   **Flexible Header Recognition:** Maps common CSV column header variations (e.g., "Author", "Authors", "author") to standard BibTeX fields.
*   **Automatic Reference Type Guessing:** Attempts to determine the BibTeX entry type (e.g., `article`, `book`, `incollection`, `misc`) based on the columns present in the CSV.
*   **Key Requirement:** Enforces the presence of a "key" column in the CSV for unique BibTeX entry identifiers.
*   **Custom Delimiter:** Supports CSV files with delimiters other than a comma (e.g., semicolon).
*   **URL Handling:** Automatically formats URLs in the `howpublished` field using `\url{}`.
*   **Multiple Authors/Editors:** Handles multiple authors/editors in a single field if they are separated by a semicolon (`;`).
*   **Warning for Unrecognized Columns:** Informs the user about CSV columns that are not mapped to any BibTeX field.
*   **Attribute Filtering:** Only includes attributes allowed for the guessed BibTeX entry type.

## Prerequisites

*   Python 3.x

## Installation

No special installation is required. Simply download or clone the `csv2bib.py` script to your local machine.

```bash
git clone <your-repo-url> # or just download the csv2bib.py file
cd <your-repo-directory>
