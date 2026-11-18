# Outstanding Cleaner

A browser-based tool for cleaning, filtering, sorting, and organizing insurance premium outstanding reports into a more readable format.

## Overview

Outstanding Cleaner was developed to simplify the handling of premium outstanding reports within a specific insurance workflow. Raw outstanding reports can contain many records, making it difficult to quickly identify and organize relevant entries. This tool streamlines that process by filtering qualifying records, sorting them by outstanding amount, and presenting the results in a cleaner format for review and export.

The application works with Excel reports and allows users to export the cleaned results into Excel and PDF formats.

## Features

* **Excel file upload:** Upload reports using drag-and-drop or the file picker.
* **Automatic filtering:** Filters records based on predefined criteria.
* **Outstanding amount sorting:** Arranges records from highest outstanding amount to lowest.
* **Branch organization:** Groups records by branch code, with smaller groups consolidated into an "Other branches" section.
* **Data preview:** Preview cleaned records before exporting.
* **Excel export:** Download the processed report in Excel format.
* **PDF export:** Generate a PDF version of the cleaned report.

## How It Works

The application processes uploaded Excel reports using predefined rules to identify qualifying records. Records are retained when they meet the following conditions:

* The branch code is numeric and contains at least six digits.
* The policy number in Column C begins with `P/`.
* The outstanding amount in Column K is greater than zero.

Qualifying records are extracted and organized using relevant fields, including:

* Branch Code
* Date
* Insured Name
* Policy Number
* Debit Number
* Premium Charged
* Outstanding Amount

Records are sorted by outstanding amount in descending order. Where outstanding amounts are equal, the earlier debit date takes priority.

Branch grouping is applied to make the report easier to navigate. Branches with five or more records are displayed separately, while smaller groups are consolidated under **Other branches**.

## How to Use

1. Open `Outstanding\_Cleaner.html` in a web browser.
2. Upload the raw premium outstanding Excel report using drag-and-drop or the file picker.
3. Allow the tool to process and filter the records.
4. Review the cleaned report in the preview table.
5. Export the results to Excel or PDF.

> The workbook is expected to contain the relevant data in a worksheet named `Sheet1`.



## Technologies Used

* HTML
* JavaScript
* SheetJS — Excel file reading
* ExcelJS — Excel report generation
* jsPDF — PDF generation
* jsPDF AutoTable — PDF table formatting

## Project Purpose

This project was built to address a practical reporting task encountered in an insurance operations workflow. It demonstrates the use of browser-based tools to automate repetitive data handling, reduce manual report organization, and make operational data easier to review.

## Limitations

* The tool is designed around a specific report structure and predefined column positions.
* It is tailored to this outstanding report format and is not intended to process every type of outstanding report.
* It expects the worksheet name `Sheet1`.
* Filtering rules are fixed within the application and may need adjustment if the source report format changes.

## Disclaimer

This is a workflow-specific utility developed for learning and operational automation purposes. It is not an official SIC Insurance PLC product or a general-purpose insurance reporting platform.

Do not publish actual customer records, policy details, confidential company information, or internal credentials. Use anonymized or dummy data for screenshots and demonstrations.

## Author

**Kelvin Asare-Baffour**  
Data Engineer

