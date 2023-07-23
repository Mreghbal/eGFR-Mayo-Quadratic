# Estimated Glomerular Filtration Rate (eGFR) Calculator

## Table of Contents
- [Introduction](#introduction)
- [Explanation](#explanation)
- [Usage](#usage)
  - [Prerequisites](#prerequisites)
  - [Running the Code](#running-the-code)
  - [Input Validation](#input-validation)
  - [Interpreting the Results](#interpreting-the-results)
- [Follow Me](#follow-me)

## Introduction
The Estimated Glomerular Filtration Rate (eGFR) is a measure used in clinical practice to assess kidney function. It estimates the rate at which the kidneys filter waste products from the blood. The eGFR value is an important indicator for diagnosing and monitoring various kidney diseases.

This repository contains a Python code that calculates the eGFR using the Mayo Quadratic equation. The code takes into account the patient's age, serum creatinine level, and gender to provide an estimate of the eGFR.

## Explanation
The eGFR calculation is based on the Mayo Quadratic equation, which incorporates the patient's age, serum creatinine level, and gender. The equation is as follows:

```
eGFR = 186 * (serum_creatinine ** (-1.154)) * (age ** (-0.203)) * adjustment_factor
```

The adjustment factor depends on the patient's gender. For males, the adjustment factor 1.0, while for females, it is 0.742.

The eGFR result represents the estimated kidney function in milliliters per minute per 1.73 square meters (mL/min/1.73m²). Higher eGFR values indicate better kidney function.

## Usage
To use the eGFR calculator, follow the steps below.

### Prerequisites
- Python 3.x installed on your system

### Running the Code
1. Clone this repository to your local machine or download the code as a ZIP file.
2. Open a terminal or command prompt and navigate to the directory where the code is located.
3. Run the following command to execute the code:
   ```
   python egfr_calculator.py
   ```
4. Follow the prompts to enter the required information:
   - Enter the patient's age: [Enter the patient's age in years]
   - Enter serum creatinine level (mg/dL): [Enter the patient's serum creatinine level]
   - Enter patient's gender (M/F): [Enter 'M' for male or 'F' for female]
5. The code will calculate the eGFR using the provided inputs and display the result if it is valid.

### Input Validation
The code performs basic input validation to ensure that the entered values are valid for the calculation. It checks the following conditions:
- Age and serum creatinine must be positive numbers. If either value is less than or equal to zero, an error message is displayed.

### Interpreting the Results
If the eGFR calculation is successful and the result is not None, the code will display the estimated Glomerular Filtration Rate (eGFR) in mL/min/1.73m² units. The result is rounded to two decimal places.

It's important to note that the eGFR is just an estimate and should be interpreted in conjunction with other clinical information. Consult a healthcare professional for a comprehensive evaluation of kidney function.

## Follow Me
If you find this code useful, consider following me on LinkedIn and Twitter for more updates and resources.

LinkedIn: [Reza Eghbal](https://www.linkedin.com/in/mreghbal)

Twitter: [Reza Eghbal](https://twitter.com/mreghbal)
