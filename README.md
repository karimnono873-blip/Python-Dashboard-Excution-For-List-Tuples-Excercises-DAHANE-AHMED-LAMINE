# 🐍 Python Data Structures Studio

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Python Algorithms](https://img.shields.io/badge/Python_Data_Structures-3776AB?style=for-the-badge&logo=python&logoColor=white)

> **An interactive, browser-based IDE simulator designed to teach and demonstrate fundamental Python data structures and algorithms.**

## 📖 Overview

This project is an educational web application that simulates a Python execution environment. It was built to solve and demonstrate a series of practical programming exercises focused on manipulating core Python data structures: **Lists, Dictionaries, Tuples, and Sets**.

Instead of presenting static code snippets, this repository features a **Single-Page Application (SPA)** that acts as a code playground. Users can navigate through different algorithm challenges, read the Python source code with custom syntax highlighting, and click "Run Script" to see the output in a simulated web terminal.

---

## ✨ Key Features

* 💻 **Simulated Web Terminal:** A custom JavaScript-based terminal that mimics Python console output, complete with execution delays and exit codes.
* 🎨 **IDE Aesthetic:** A responsive, dark-mode user interface inspired by modern code editors (like VS Code and GitHub Codespaces).
* 📝 **Custom Syntax Highlighting:** Pure CSS-driven syntax highlighting for Python keywords, functions, strings, and comments.
* ⚡ **Zero Dependencies:** Built entirely with Vanilla JavaScript, HTML5, and CSS3. No backend server or Python runtime is actually required to view the demonstrations.

---

## 🧠 Python Exercises Demonstrated

The dashboard includes the source code and execution results for the following 6 challenges:

1. **List Operations:** A function to multiply all numerical items within a list.
2. **Tuple Sorting (Lambda):** Sorting a list of tuples in increasing order based on the last element of each tuple.
3. **Dictionary Combination:** Merging two dictionaries and mathematically adding the values of intersecting keys using `collections.Counter`.
4. **Dictionary Comprehension:** Generating a dictionary of squares `{i: i*i}` for a given integral number `n`.
5. **Float Sorting:** Parsing and sorting a list of tuples based on a string-formatted float element in descending order.
6. **Set Manipulations:** Creating sets, iterating over them, and safely adding/removing members using `.add()`, `.remove()`, and `.discard()`.

---

## 🚀 Quick Start

Because this simulator is built entirely with frontend technologies, it is incredibly easy to run.

1. Clone or download this repository.
2. Locate the `python_data_structures.html` file.
3. **Double-click** to open it in any modern web browser (Chrome, Edge, Firefox, Safari).
4. Use the left sidebar to navigate between the different Python exercises.
5. Click **"▶ Run Script"** on any active tab to watch the simulated terminal output the results.

---

## 💻 Sample Code Highlight

**Objective:** *Write a Python program that combines two dictionaries by adding values for common keys.*

```python
from collections import Counter

def combine_dicts(dict1, dict2):
    """Combines two dicts, adding values of common keys using Counter."""
    # Counter naturally adds values for intersecting keys when using '+'
    combined = Counter(dict1) + Counter(dict2)
    # Convert back to standard dictionary
    return dict(combined)

d1 = {'a': 100, 'b': 200, 'c': 300}
d2 = {'a': 300, 'b': 200, 'd': 400}

result = combine_dicts(d1, d2)
print(f"Expected result: {result}")
# Output: {'a': 400, 'b': 400, 'c': 300, 'd': 400}
