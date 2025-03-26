# akansha_assignment
# PDF Table Extraction and Decryption

This project provides a Python-based solution to extract tables from PDF files using `pdfplumber` and `pandas`. It also includes functionality to handle and decrypt encrypted PDF content using a custom decryption method.

## Features
- Extract tables from PDF files into Excel files.
- Handle unstructured table data by extracting and formatting text.
- Decrypt and extract tables from encrypted PDFs.
- Save extracted data to Excel with multiple sheets for each table.

## Prerequisites
Ensure you have the following installed:
- Python 3.7+
- `pdfplumber`
- `pandas`
- `openpyxl`

You can install these dependencies using:
```bash
pip install pdfplumber pandas openpyxl
```

## Usage

### Extracting Tables from PDF
```python
extract_tables_from_pdf("path_to_input.pdf", "output_file.xlsx")
```
- **path_to_input.pdf**: Path to the PDF file.
- **output_file.xlsx**: Path to save the extracted tables in an Excel file.

### Handling Encrypted PDFs
```python
handle_encrypted_pdf("path_to_encrypted_pdf.pdf", "output_file.xlsx")
```
- **path_to_encrypted_pdf.pdf**: Path to the encrypted PDF.
- **output_file.xlsx**: Path to save the decrypted tables in an Excel file.

## Functions
### `extract_tables_from_pdf(pdf_path, output_excel_path)`
- Extracts tables from the PDF using `pdfplumber`.
- Extracts unstructured text if tables are not detected.
- Saves the results to an Excel file with each table on a separate sheet.

### `decrypt_values(value)`
- Attempts to decrypt encrypted values using character decoding.

### `handle_encrypted_pdf(pdf_path, output_excel_path)`
- Extracts and decrypts tables using the custom decryption method.
- Exports the decrypted tables to Excel.

## Error Handling
- The code prints error messages if it encounters issues while processing pages.
- If no tables are found, it displays a message instead of generating an Excel file.


