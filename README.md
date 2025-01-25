# Bill-Extraction-and-Aggregation
An intelligent application to extract structured data from invoices and bills, enabling seamless data management for finance and accounting workflows.

Features
PDF and Image Extraction: Extract text from PDF files and image-based invoices using PyPDF2 and Tesseract OCR.
Structured Data Output: Automatically organizes invoice data, including:
Invoice number
GST number
Invoice date
Product details (name, quantity, price, tax rates, etc.)
GST Calculation: Calculates SGST, CGST, IGST, total GST rate, total GST amount, and grand total for each product.
Date Normalization: Converts invoice dates to a standard format (DD/MM/YYYY).
Customizable UI: Uses Streamlit to create a user-friendly interface with interactive buttons and modern CSS styling.
Excel Export: Saves extracted data into a clean and structured Excel file.
Technologies Used
Programming Language: Python
OCR Library: pytesseract
Web Framework: Streamlit
Data Handling: Pandas
Excel File Handling: openpyxl
Google Generative AI: For AI-powered data enhancement
Image Handling: Pillow
PDF Parsing: PyPDF2
Text Processing: Spacy
Installation
Prerequisites
Python Version: Ensure Python 3.9 or above is installed.

Install Dependencies: Clone the repository and install required libraries by running the following command in the project directory:

pip install -r requirements.txt
Tesseract OCR: You need to install Tesseract OCR to process images:

Download and install Tesseract from here.
Add the Tesseract path to your environment variables or specify it directly in the script:
pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
Google Generative AI API Key:

To integrate AI-powered data refinement, configure your API key for Google Generative AI by setting it in the script:
genai.configure(api_key="YOUR_API_KEY")
Configuration
Before running the application, you may need to adjust the following configuration settings:

Tesseract Path: Make sure Tesseract is properly configured for your system:

pytesseract.tesseract_cmd = r'C:\Path\To\Tesseract\tesseract.exe'
Excel File Path: Set the path where the extracted data will be stored:

EXCEL_FILE_PATH = 'path_to_save_data/eng.xlsx'
Google API Key: Set your Google API key for data enhancement:

genai.configure(api_key="YOUR_API_KEY")
Usage
Run the Application: Launch the Streamlit application by running:

streamlit run app.py
Upload Invoice: Upload invoices in PDF or image format via the web interface.

Extract Data: The application will extract structured data (e.g., invoice number, GST number, product details) from the uploaded file.

View Results: Extracted data will be displayed on the Streamlit interface and appended to an Excel file (eng.xlsx).

Download Files: You can download the Excel file containing the extracted data or the monthly summary.
