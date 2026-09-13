TASK 5
# Enterprise Python Automation Capstone Project

## Automated API-Based Report Generator

## Overview

The Automated API-Based Report Generator is an enterprise-oriented Python automation project that combines API data retrieval, data processing, report generation, file persistence, command-line execution, error handling, and scheduling.

The application retrieves data from a public API, analyzes the collected information, generates summary statistics, and produces machine-readable JSON files and a PDF report.

The project demonstrates how multiple Python components can be integrated into a simple automated business workflow.

## Features

* Public API integration.
* Automated data retrieval.
* Request timeout handling.
* Data processing.
* Statistical analysis.
* JSON data storage.
* PDF report generation.
* Command-line interface.
* Scheduled execution.
* Error handling.
* Automated workflow.

## API Used

The project uses the JSONPlaceholder API:

```text
https://jsonplaceholder.typicode.com/posts
```

The API provides sample post data that can be retrieved and processed by the application.

## Technologies Used

* Python
* Requests
* ReportLab
* JSON
* Schedule
* Argparse
* Datetime

## How It Works

The application follows an automated pipeline:

```text
Public API
    ↓
Data Retrieval
    ↓
Data Processing
    ↓
Statistical Analysis
    ↓
JSON Storage
    ↓
PDF Report Generation
    ↓
Automated Output
```

## Data Processing

The application retrieves post records from the API and calculates summary information including:

* Total number of records.
* Number of unique users.
* Most active user.
* Report generation timestamp.

## Generated Files

The application generates:

```text
raw_data.json
summary.json
automated_report.pdf
```

### `raw_data.json`

Contains the data retrieved from the API.

### `summary.json`

Contains the calculated analytical summary.

### `automated_report.pdf`

Contains a human-readable PDF report generated automatically by Python.

## PDF Report

The PDF report contains information such as:

```text
Automated API Report

Generated At: ...
Total Records: ...
Unique Users: ...
Most Active User: ...
```

## Command-Line Interface

The application provides a command-line option for generating the report.

Example:

```bash
python cli.py --generate
```

The command starts the report generation workflow.

## Scheduling

The project uses the Python `schedule` library to demonstrate automated execution.

Example:

```python
schedule.every(1).hours.do(scheduled_job)
```

This allows the report-generation function to be scheduled at regular intervals.

## Error Handling

The application includes exception handling for:

* API request failures.
* Network-related errors.
* Unexpected processing errors.

This prevents common runtime failures from terminating the entire workflow without an informative message.

## Running the Project

Install the required libraries:

```bash
pip install requests reportlab schedule
```

Run the report generator:

```bash
python report_generator.py
```

Or use the command-line interface:

```bash
python cli.py --generate
```

## Example Output

```text
Starting automated report generation...
Downloaded 100 records.
Report generation completed successfully.

SUMMARY
========================================
total_records: 100
unique_users: 10
most_active_user: ...
generated_at: ...
```

The exact output values are generated from the API response at execution time.

## Project Objectives

* Integrate a public API into a Python application.
* Automate data collection and processing.
* Generate machine-readable and human-readable reports.
* Develop a command-line interface.
* Implement scheduling.
* Practice error handling.
* Understand enterprise-style automation workflows.
* Combine multiple Python technologies into a single application.

## Applications

Automated reporting systems can be used in business analytics, operational monitoring, data processing, administrative workflows, and periodic report generation.

The project can be further extended to support databases, email delivery, dashboards, cloud deployment, multiple APIs, and more advanced analytics.

## Author

M. Ayshwarya
