# SGPA, CGPA & Class Performance Index Calculator

A menu-driven Python CLI tool designed for students and educators to calculate Semester Grade Point Average (SGPA), Cumulative Grade Point Average (CGPA), and an overall Class Performance Index (CPI).

## Features

* **SGPA Calculator:** Computes single-semester SGPA using subject-wise credits and grade points (0–10 scale).
* **CGPA Calculator:** 
  * Supports direct entry of semester SGPAs/credits or step-by-step calculation from individual subjects.
  * Converts CGPA to an approximate percentage (default multiplier: `9.5`).
  * Compares current CGPA against a target/required CGPA to show surplus or deficit points.
* **Class Performance Index (CPI):**
  * Calculates class average, highest/lowest GPA, pass percentage, and distinction rate.
  * Generates a weighted **CPI score (out of 100)** with an overall performance rating (*Outstanding*, *Very Good*, *Good*, *Average*, *Needs Improvement*).
  * Outputs a sorted **Rank List** indicating Pass/Fail status for each student.
* **Input Validation:** Built-in error handling ensures valid numeric ranges and prevents crashes from invalid entries.

## Getting Started

### Prerequisites
* Python 3.x (No external libraries required)

### Running the Script
1. Clone the repository or download the `.py` / `.ipynb` file.
2. Run the program in your terminal or Google Colab:
   ```bash
   python main.py
   ```

## Configuration

You can customize university-specific grading rules at the top of the script:

```python
AVERAGE_WEIGHT = 0.7      # Weight given to class average GPA in CPI
PASS_WEIGHT = 0.3         # Weight given to pass percentage in CPI
DISTINCTION_GPA = 8.0     # Minimum GPA required for distinction
PERCENTAGE_FACTOR = 9.5   # Multiplier used for CGPA-to-percentage conversion
```

## Formulas Used

* **SGPA** = \(\frac{\sum (\text{Subject Credits} \times \text{Grade Point})}{\sum \text{Subject Credits}}\)
* **CGPA** = \(\frac{\sum (\text{Semester SGPA} \times \text{Semester Credits})}{\sum \text{Semester Credits}}\)
* **CPI** = (0.7 × Class Average GPA × 10) + (0.3 × Pass Percentage)

## Example Output

```text
========== CLASS REPORT ==========
Class: 71
Total Students: 30
Class Average GPA: 6.53
Highest GPA: 10.0
Lowest GPA: 0.0
Passed: 25 ( 83.3 %)
Distinction: 12 ( 40.0 %)

CLASS PERFORMANCE INDEX: 70.73 / 100
Rating: Good
```
