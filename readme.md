# PythonTeX LaTeX Integration

A powerful project that combines the computational capabilities of Python with the typesetting excellence of LaTeX using the PythonTeX module. This integration allows you to embed Python code directly within LaTeX documents, enabling dynamic data calculation, chart generation, and seamless data export to Google Sheets and Excel files.

## Features

- **Dynamic Data Processing**: Execute Python code directly within LaTeX documents
- **Chart Generation**: Create and embed charts dynamically using Python plotting libraries
- **Data Export**: Save processed data to Google Sheets and Excel files
- **Real-time Calculations**: Perform calculations on-the-fly during document compilation
- **Module Integration**: Import and use any Python module within your LaTeX documents

## Prerequisites

- Linux-based system (Ubuntu/Debian recommended)
- LaTeX distribution (TeX Live)
- Python 3.x
- Virtual environment support

## Installation

Follow these steps to set up your environment:

### 1. System Updates and Dependencies
```bash
sudo apt update
sudo apt install texlive
```

### 2. Python Virtual Environment Setup
```bash
virtualenv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Usage

### Compiling Documents

To execute the sample projects, navigate to any sample folder and run the following commands in sequence:

```bash
# Initial LaTeX compilation
pdflatex -interaction=nonstopmode doc.tex

# Execute embedded Python code
pythontex doc.tex

# Final LaTeX compilation with Python results
pdflatex -interaction=nonstopmode doc.tex
```

### Google Sheets Integration

For Google Sheets functionality (available in sample2):

#### Option 1: Use Your Own Service Account
1. Create a Google Cloud Project
2. Enable Google Sheets API
3. Create a service account and download the JSON key
4. Rename credential to `service_account.json` and place it in sample2 folder
5. Replace `SPREADSHEET_ID` with your sheet id
6. In your sheet give access to your email

#### Option 2: Share with Existing Service Account
1. Ask me for credential.
2. Share your Google Sheet with the following email address:
```
latex-python@latex-python.iam.gserviceaccount.com
```
3. Change `SPREADSHEET_ID` with your sheet id

#### Option 3: Use Existing Sheet
1. Ask me for credential.
2. See the results in `https://docs.google.com/spreadsheets/d/1kSz21B5faifZ6JYvH_2wdvosoQVhP1f1XnYEoo9olzk/`

## Project Structure

```
├── sample1/                    # Basic PythonTeX example
│   └── doc.tex                 # Sample LaTeX document
├── sample2/                    # Google Sheets integration 
│   ├── doc.tex                 # Sample with Google Sheets
│   └── service_account.json    # Google API credentials
├── requirements.txt            # Python dependencies
├── proj.ipynb                  # A demonstration of openpyxl abilities 
└── README.md                   # This file
```

## Workflow

1. **Write**: Create LaTeX documents with embedded Python code blocks
2. **Process**: Run the compilation sequence to execute Python code
3. **Generate**: Python calculations and charts are automatically integrated
4. **Export**: Data is saved to Google Sheets/Excel as configured
5. **Output**: Final PDF with dynamic content and updated data
