# Day 33 – Python Coding Challenge

A set of beginner-friendly Python problems focused on `while` loops, `for` loops, and conditional logic, split into two levels: **placement-style thinking** and **real-world data analyst scenarios**.

## Files

| File | Description |
|------|-------------|
| `Day33_Coding_Challenge.pdf` | Problem statements |
| `Day-33-Data-analytics-challenge-python.ipynb` | Jupyter Notebook with solutions and sample output |

## Requirements

- Python 3.9+
- Jupyter Notebook or JupyterLab

```bash
pip install notebook
jupyter notebook Day-33-Data-analytics-challenge-python.ipynb
```

---

## Level 1: Placement Thinking

### 1. Number Guessing Game
**Concept:** infinite `while` loop + `if`

A secret number (`7`) is stored and the user guesses it.
- Guess lower than the secret → prints `Too Low`
- Guess higher than the secret → prints `Too High`
- Correct guess → prints `You Won` and stops

**Example**
```
Enter any number:98
Too High
```

### 2. Reverse a Number
**Concept:** `while` loop, modulo (`%`) and floor division (`//`)

Reverses the digits of an integer by repeatedly extracting the last digit (`num % 10`), appending it to the result (`res * 10 + digit`), and dropping it from the input (`num // 10`).

**Example**
```
Input:  1234  →  Output: 4321
Input:  78910 →  Output: 1987   (the leading zero is dropped because the result is an integer)
```

### 3. Count Digits in a Number
**Concept:** repeated division by 10

Counts how many times a number can be divided by 10 before reaching 0.

**Example**
```
Input:  12345  →  Output: 5
```

---

## Level 2: Real-World Scenario (Data Analyst Thinking)

### 4. Sales Threshold Checker
**Concept:** loop + condition filtering

Given `sales = [1200, 800, 1500, 400, 2000]`, the program:
- Prints only the sales greater than 1000
- Prints how many such sales exist

**Output**
```
sales grater than 1000: [1200, 1500, 2000]
Count of sales grater than 1000: 3
```

### 5. Continuous Data Entry System
**Concept:** `while True` with a sentinel value

Keeps asking the user for numbers and stops when `0` is entered, then prints the running total. This mimics how real systems collect streaming data.

**Example**
```
Enter number:1
Enter number:2
...
Enter number:0
Total sum of the entered numbers: 25
```

---

## Concepts Practiced

- `while` loops (including `while True` with `break`)
- `for` loops and list iteration
- `if` / conditional filtering
- Integer arithmetic: `%` and `//`
- Taking user input with `input()` and converting with `int()`
- Building and counting results with lists (`append`, `len`)

## Known Limitations / Ideas for Improvement

- **Guessing game:** the input is read once, before the loop, so the user only gets a single guess. Moving `input()` inside the loop (and `break`ing only on a correct guess) gives the intended repeated-guess behavior.
- **Reverse / count digits:** negative numbers are not handled. Use `abs(num)` to support them.
- **Input validation:** non-numeric input will raise a `ValueError`. Wrapping `int(input(...))` in `try/except` would make the programs more robust.

## Author

Day 33 of my Python / Data Analytics learning journey.
