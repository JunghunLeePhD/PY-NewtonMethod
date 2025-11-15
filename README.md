# Computing Irrational Numbers: An Interactive Guide to Root-Finding 📚

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPOSITORY/blob/main/YOUR_NOTEBOOK_FILE.ipynb)

> **Note:** To get the Colab link above to work, you must:
> 1.  Save this file as a Jupyter Notebook (e.g., `Root_Finding_Tutorial.ipynb`).
> 2.  Upload it to a GitHub repository.
> 3.  Edit this README file and replace `YOUR_USERNAME`, `YOUR_REPOSITORY`, and `YOUR_NOTEBOOK_FILE.ipynb` with your project's details.

---

This repository contains a single, comprehensive Python notebook file that serves as an interactive tutorial. It explores the concept of computing irrational numbers (like $\sqrt{2026}$) by treating them as the **roots of functions**.

This document is designed to be read from top to bottom. It blends foundational mathematical theory with practical, executable Python code snippets that visualize and solve the very concepts being explained.

## 🎯 Project Purpose

The goal of this project is not to provide a library, but to offer a self-contained educational experience that answers:

1.  **What *are* irrational numbers, really?** (The Algebraic Foundations)
2.  **How can we *find* them?** (The Numerical Methods)
3.  **How can we *implement* these methods?** (The Python Code)

By the end, you will have a deep, practical understanding of the **Bisection Method** and the **Newton-Raphson Method**, two of the most fundamental algorithms in numerical analysis.

---

## 📖 Key Concepts Covered

The tutorial is broken down into four main sections:

### 1. Algebraic Foundations (The "Why")
* **Rings vs. Fields:** A simple introduction to the algebraic structures of Integers ($\mathbb{Z}$) and Rational Numbers ($\mathbb{Q}$).
* **Polynomials:** Understanding what it means for a polynomial to be "defined over" a ring or field.
* **The Emergence of Irrationality:** How polynomials with simple rational coefficients (like $x^2 - 2 = 0$) can produce irrational roots ($\sqrt{2}$).
* **Algebraic vs. Transcendental Numbers:** Defining the landscape of numbers.

### 2. Numerical Root-Finding Theory (The "How")
* **The Canonical Problem:** How $f(x) = 0$ is the universal target for many math problems.
* **Bracketing vs. Open Methods:** The two main philosophies for finding roots.
* **Bisection Method:** A deep dive into the algorithm, its theoretical foundation (Intermediate Value Theorem), and its predictable **linear convergence**.
* **Newton-Raphson Method:** The geometric intuition (tangent lines), the iterative formula, and its famously fast **quadratic convergence** (and its pitfalls).
* **Comparison:** A nuanced look at Speed vs. Stability vs. Cost, including a brief mention of the Secant Method.

### 3. Python Basics (The "Tools")
* **Lambda Functions:** A quick introduction to `lambda` (anonymous functions) for defining simple math functions on the fly.
* **Matplotlib & NumPy:** A "4-Step Process" for plotting functions to visualize the concepts.

### 4. Practical Implementation (The "Code")
This is the core of the tutorial, with executable code blocks that:
* **Implement the Bisection Method** using `lambda` functions.
* **Geometrically visualize** the Bisection Method, showing the "box" shrinking.
* **Implement the Newton-Raphson Method** using its derivative.
* **Geometrically visualize** Newton's Method, showing the "tangent lines sliding" toward the root in both global and local (zoomed) views.
* **Compare Convergence:** A final plot directly compares the error rates of Bisection vs. Newton's on a log scale, demonstrating their convergence speeds empirically.

---

## 🚀 How to Use This Project

This file is designed to be run as an **interactive notebook**.

**Recommended Approach (Easiest):**
1.  Click the **"Open In Colab"** badge at the top of this file.
2.  Google Colab will open the notebook in your browser.
3.  Read the text and run the code cells (the blocks with `# Run the code below!`) in order from top to bottom.
4.  Observe the console output and the `matplotlib` plots that are generated directly in the notebook.

**Alternative (Local):**
1.  Ensure you have an environment that can run Jupyter Notebooks (like **VS Code** with the Python/Jupyter extension, **Jupyter Lab**, or **Anaconda**).
2.  Clone or download this repository.
3.  Open the notebook file.
4.  Run the code cells as you read the tutorial.

---

## 📦 Requirements

If you run this in **Google Colab, all requirements are pre-installed.**

If you run this locally, you will need **Python 3** and the following libraries:

* **NumPy:** For numerical operations and generating data for plots.
* **Matplotlib:** For visualizing the functions and algorithms.

You can install them using `pip`:
```bash
pip install numpy matplotlib
```
