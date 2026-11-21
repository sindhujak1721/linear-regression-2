# Logistic Regression Using Python – FDP Hands-on Activity

## 1. Project Overview

This project demonstrates **Logistic Regression**, a Supervised Machine Learning algorithm used for classification problems.

In this hands-on activity, we build a Logistic Regression model to predict whether a student will Pass or Fail based on the number of hours studied.

The project also demonstrates the mathematical concept of the **Sigmoid Function**, which converts a calculated value into a probability between 0 and 1.

## 2. Objectives

- Understand the fundamentals of Logistic Regression.
- Learn the difference between classification and regression.
- Create a simple student pass/fail prediction model.
- Train a Logistic Regression model using Scikit-learn.
- Understand the Sigmoid Function.
- Calculate classification probabilities.
- Apply a threshold to make predictions.

## 3. Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Scikit-learn | Machine Learning model |
| Math | Mathematical calculations |
| Google Colab | Development environment |

## 4. Dataset Description

This project uses a small sample dataset created directly in the Python program.

### Input Data

```python
X = [[1], [2], [3], [4], [5], [6]]
```

The input represents the number of hours studied by students.

### Output Data

```python
y = [0, 0, 0, 1, 1, 1]
```

| Study Hours | Result | Meaning |
|---|---|---|
| 1 | 0 | Fail |
| 2 | 0 | Fail |
| 3 | 0 | Fail |
| 4 | 1 | Pass |
| 5 | 1 | Pass |
| 6 | 1 | Pass |

**Note:**
- 0 represents Fail.
- 1 represents Pass.

## 5. Project Workflow

### Step 1: Import Required Libraries

```python
from sklearn.linear_model import LogisticRegression
```

Import Logistic Regression from Scikit-learn.

### Step 2: Create the Dataset

```python
X = [[1], [2], [3], [4], [5], [6]]
y = [0, 0, 0, 1, 1, 1]
```

Define study hours as the input and student results as the output.

### Step 3: Create the Model

```python
model = LogisticRegression()
```

Create a Logistic Regression model.

### Step 4: Train the Model

```python
model.fit(X, y)
```

Train the model using the sample dataset.

### Step 5: Predict Student Results

```python
prediction = model.predict([[4]])
```

Predict whether a student who studied 4 hours will pass or fail.

### Step 6: Display the Result

```python
if prediction[0] == 1:
    print("Student will Pass")
else:
    print("Student will Fail")
```

Display the predicted classification result.

## 6. Understanding the Sigmoid Function

The Sigmoid Function is an important mathematical function used in Logistic Regression.

It converts any real-valued input into a probability between 0 and 1.

### Mathematical Formula

**Sigmoid Function:**

\[
\sigma(z)=\frac{1}{1+e^{-z}}
\]

Where:

- z = Linear combination of input and coefficients.
- e = Euler's mathematical constant.
- σ(z) = Predicted probability.

### Step 1: Define the Values

```python
import math

b0 = -5
b1 = 1.2
x = 5
```

### Step 2: Calculate Z

```python
z = b0 + (b1 * x)
```

Formula:

\[
z=b_0+b_1x
\]

Substituting the values:

\[
z=-5+(1.2\times5)=1
\]

### Step 3: Apply the Sigmoid Function

```python
probability = 1 / (1 + math.exp(-z))
```

The calculated probability is approximately 0.7311.

### Step 4: Classification

```python
if probability >= 0.5:
    print("Student will Pass")
else:
    print("Student will Fail")
```

The classification threshold is 0.5.

- Probability greater than or equal to 0.5 → Pass.
- Probability less than 0.5 → Fail.

## 7. Expected Output

### Model Prediction

```text
Student will Pass
```

### Sigmoid Function Output

```text
Z value: 1.0
Probability: 0.7310585786300049
Student will Pass
```

*The Logistic Regression model's prediction and the manually calculated sigmoid demonstration are separate examples in this program.*

## 8. How to Run the Project

### Option 1: Google Colab

1. Open https://colab.research.google.com/
2. Create a new notebook.
3. Upload `logistic_regression_20_11_2026.py` or copy the Python code.
4. Run the program.
5. Observe the prediction and sigmoid probability.

### Option 2: VS Code

1. Install Python.
2. Open VS Code.
3. Create a Python file named `logistic_regression.py`.
4. Copy the uploaded Python code into the file.
5. Install Scikit-learn:

```bash
pip install scikit-learn
```

6. Run the program:

```bash
python logistic_regression.py
```

## 9. Hands-on Practice Activities

1. Change the study hours from 4 to 5 and observe the prediction.
2. Predict the result for a student who studied 2 hours.
3. Add more student records to the dataset.
4. Change the classification threshold from 0.5 to 0.7 in the sigmoid example.
5. Calculate the sigmoid probability for z = 2.
6. Experiment with different values of b0 and b1.
7. Create a program to predict whether a student passes or fails based on study hours.

## 10. Learning Outcomes

After completing this activity, participants will be able to:

- Understand Logistic Regression.
- Identify classification problems.
- Train a classification model using Scikit-learn.
- Predict binary outcomes.
- Understand the Sigmoid Function.
- Calculate probabilities.
- Apply classification thresholds.

## 11. Conclusion

This hands-on activity introduces Logistic Regression through a simple student pass/fail prediction problem.

Participants learn how to create and train a Machine Learning classification model using Python and understand how the Sigmoid Function converts mathematical values into probabilities.

**Activity:** Faculty Development Programme (FDP) – Hands-on Machine Learning

**Topic:** Logistic Regression Using Python

**Domain:** Artificial Intelligence and Data Science
