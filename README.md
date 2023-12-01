# README for Data Validation Project

## Overview
This project is designed to validate CSV files using a Python script. It checks for common data issues such as carriage returns, unnamed columns, and columns with zero counts. The script is integrated with MLflow for tracking and logging metrics during the validation process.

## Requirements
- Python 3.x
- MLflow
- Pandas
- Click (for command-line interface)

## Installation
1. Ensure Python 3.x is installed on your system.
2. Install the required Python libraries:
   ```bash
   pip install mlflow pandas click
   ```

## Usage
The script can be executed from the command line with the following arguments:

- `metrics`: A boolean value indicating whether to log metrics to MLflow.
- `max_errors`: An integer specifying the maximum number of errors to tolerate.
- `filename`: The path to the CSV file to be validated.

Run the script using the command:

```bash
python main.py [metrics] [max_errors] [filename]
```

Replace `[metrics]`, `[max_errors]`, and `[filename]` with appropriate values.

### Example
```bash
python main.py True 10 /path/to/your/file.csv
```

## Features
- **Carriage Return Detection**: Identifies carriage returns within any field of the CSV file.
- **Unnamed Column Detection**: Counts and reports columns with 'Unnamed' in their header.
- **Zero Count Column Detection**: Identifies columns that have no data entries.

## MLflow Integration
When the `metrics` flag is set to `True`, the script logs the following metrics to MLflow:
- Number of unnamed columns.
- Number of zero count columns.

## Output
The script outputs warnings to the console for the following issues:
- Columns with no data entries.
- Unnamed columns.
- Fields containing carriage returns, along with their location in the CSV file.

## Contributing
Contributions to this project are welcome. Please ensure that any pull requests or issues are concise and clear in intent.
