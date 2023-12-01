# Week12 mini project - MLflow to manage a simple machine learning project

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
## Running the MLproject and Output

### Initial Testing with a Faulty CSV File
Start by running the project using a CSV file known to contain validation errors. This test helps to ensure that our validation script correctly identifies and reports issues within the CSV file.

Execute the following command in your terminal:

```bash
mlflow run . -P filename=carriage.csv
```
<img width="745" alt="Screenshot 2023-11-19 at 15 17 30" src="https://github.com/nogibjj/mini-proj12-rc/assets/123079408/3231d4cb-0cfb-42a9-bcef-bfb9d1fbbf51">



**Command Result**: Observe the results for `carriage.csv`, which should display various warnings indicative of the data issues present in the file.

### Validating with a Correct CSV File
After confirming that the script effectively detects errors, proceed to test it with a well-structured, error-free CSV file. This step is crucial for verifying that the script handles valid data correctly without raising false alarms.

Run the command:

```bash
mlflow run . -P filename=wine-ratings.csv
```
<img width="748" alt="Screenshot 2023-11-19 at 15 17 54" src="https://github.com/nogibjj/mini-proj12-rc/assets/123079408/dfaba8d3-4e00-45a7-a101-b7a77099831e">


