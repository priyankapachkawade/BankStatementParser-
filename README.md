# Bank Statement Parser

A Python project for extracting, parsing, and organizing transaction data from bank statement PDFs into an SQLite database and a JSON format. This tool is designed to accommodate varying bank statement formats using a configurable parsing logic, making it adaptable across different banks.

## Features
- **PDF Text Extraction**: Extracts text data from PDF bank statements.
- **Data Parsing**: Identifies and cleans transaction data from the extracted text.
- **Configurable Parsing Logic**: Allows for parsing configurations via a config file to support different bank formats.
- **Database Storage**: Saves parsed transactions to an SQLite database in a structured format.
- **JSON Output**: Generates a JSON file with transaction data for easy access and integration.

## Project Structure
- **`BankStatementParser.ipynb`**: Contains the main code for the project, including text extraction, parsing logic, and data storage.
- **`config.json`**: Configuration file (if applicable) to manage column mapping and parsing adjustments.
- **`transaction_output.JSON`**: Sample JSON output file containing parsed transaction data.

## Database Schema
The SQLite database (`bank.db`) contains a single table (`transactions`) with the following schema:
- **unique_id**: UUID (Unique identifier for each transaction)
- **date**: Date of the transaction
- **description**: Description of the transaction
- **amount**: Transaction amount
- **transaction_type**: Indicates if the transaction is a `CREDIT` or `DEBIT`

## Prerequisites
- **Python 3.x**
- **Python libraries**: `PyMuPDF`, `sqlite3`, `json`, `uuid`, etc. (Refer to `requirements.txt`)

