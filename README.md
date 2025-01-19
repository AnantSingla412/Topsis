# TOPSIS Algorithm Implementation

## Overview

The **TOPSIS** (Technique for Order Preference by Similarity to Ideal Solution) method is a popular multi-criteria decision-making technique that ranks alternatives based on their proximity to the ideal best and worst solutions. This Python implementation calculates rankings for different alternatives considering custom weights and impacts.

---

## Installation

You can easily install the TOPSIS implementation via **pip**. The package is available on [PyPI](https://pypi.org/project/Topsis-Rohit-102203804/).

```bash
pip install Topsis-Anant-102203856==1.0.0
```

---

## Features

- **Custom Weights & Impacts**
- **Topsis Score & Rank Calculation**
- **Output to File**
- **Robust Input Validation**

---

## Prerequisites

- Python version 3.6 or higher
- Required libraries:
  - `pandas`
  - `numpy`
  - `pyexcel`

Install the required libraries using:

```bash
pip install pandas numpy pyexcel
```

---

## Usage

### Command-Line Usage

You can use the algorithm by running the following command:

```bash
python <script_name.py> <InputDataFile> <Weights> <Impacts> <ResultFileName>
```



### Example Command

```bash
python 102203856.py 102203856-data.xlsx "1,1,1,1,2" "+,+,-,-,+" 102203856-result.csv
```

---

## Input Data Format

The input dataset file should contain:

- The first column: names of the alternatives.
- Subsequent columns: numeric values for each criterion.

Example input data:

| Alternative | Criterion1 | Criterion2 | Criterion3 |
|-------------|------------|------------|------------|
| A1          | 250        | 16         | 12         |
| A2          | 200        | 18         | 11         |

---

## Output

The output file will include:

- **Topsis Score**: The calculated score for each alternative.
- **Rank**: The rank of each alternative based on the Topsis score.

Example output:

| Alternative | Topsis Score | Rank |
|-------------|--------------|------|
| A1          | 0.897        | 1    |
| A2          | 0.735        | 2    |

---

## Error Handling

The script includes robust error handling to ensure:

- **Correct number of parameters**: If the number of input arguments is incorrect, the user is shown a helpful message.
- **File not found**: An appropriate message is shown if the specified input file does not exist.
- **File format validation**: 
  - The input file must contain at least three columns.
  - Columns from the second to the last must contain only numeric values.
- **Weights and impacts validation**:
  - The number of weights, impacts, and columns in the dataset must match.
  - Impacts must be either `+` (maximize) or `-` (minimize).
  - Weights and impacts must be separated by commas.


