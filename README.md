# ReportLab Invoice PDF Generator

A small Python project that generates a formatted invoice PDF with
[ReportLab](https://www.reportlab.com/). The invoice includes company details,
customer information, line items, tax, totals, payment notes, and an optional
logo.

## Features

- A4 invoice layout
- Company and customer details
- Itemized billing table
- Tax and total calculations displayed in the invoice
- Optional `nn_logo.jpg` company logo
- PDF output generated as `invoice.pdf`

## Requirements

- Python 3.14 or newer
- ReportLab 5.0.1 or newer

## Installation

Using `uv`:

```bash
uv sync
```

Using `pip`:

```bash
python -m pip install -r requirements.txt
```

## Usage

Run the invoice script from the project root:

```bash
python invoice.py
```

After the script finishes, open `invoice.pdf` in the project directory.

If `nn_logo.jpg` is present in the project root, it is used in the invoice
header. If the logo is unavailable, the script falls back to displaying the
company name.

## Customization

Edit the values in [`invoice.py`](invoice.py) to customize:

- Company name, address, and contact information
- Invoice number, invoice date, and due date
- Customer billing details
- Item descriptions, quantities, prices, and tax rates
- Payment instructions and footer text
- PDF margins and table styling

The script currently writes the output to `invoice.pdf`. Change the filename
passed to `SimpleDocTemplate` if a different output path is needed.

## Project Structure

```text
.
├── invoice.py       # Invoice PDF generator
├── report.py        # Additional ReportLab example
├── simple.py        # Simple PDF example
├── requirements.txt # Runtime dependency
├── pyproject.toml   # Project metadata and uv configuration
└── uv.lock         # Locked dependency versions
```

## License

No license has been specified for this project yet.
