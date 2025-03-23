
# 🚀 AI-Powered Open-Source Code Review Agent
This Google Colab notebook explores the **brute-force method of code review** using AI, focusing on developing an **AI-powered open-source code review agent**. The notebook uses Python's built-in libraries, color highlighting, and integrates with **Google Gemini API** to perform advanced code analysis and provide feedback.

---

## 🛠️ **Installation and Setup**
To run this notebook, install the required dependencies:
```bash
!pip install colorama
!pip install requests
```

Import the necessary libraries:
```python
import difflib
from colorama import Fore, Style, init
from IPython.display import display, HTML, Markdown
import requests
import ast
```

---

## 🔍 **Features and Functionality**

### ✅ **1. Colored Code Difference Viewer**
- Compares two Python code files line by line.
- Highlights additions, deletions, and changes.
- Displays line numbers and modifications in a visually clear format.

📌 **Usage:**
```python
file1 = "/content/new_code.py"  # Path to the new code file
file2 = "/content/old_code.py"  # Path to the old code file
colored_output = get_diff(file1, file2)
display(HTML(f"{colored_output}"))
```

---

### ⚠️ **2. Bracket Balancing Checker**
- Identifies unbalanced brackets: `()`, `{}`, `[]`.
- Highlights the line numbers where unbalanced brackets occur.
- Provides detailed feedback.

📌 **Usage:**
```python
code_sample = """
def check_brackets():
    if (x > 0 {
        print("Hello")
    if (y < 5 {
        print("Error")
"""
print(check_unclosed_brackets(code_sample))
```

---

### 🚀 **3. AI-Powered Code Review with Gemini**
- Uses **Google Gemini API** for comprehensive code review.
- Detects syntax errors, logical flaws, performance issues, and best practices violations.
- Generates detailed feedback in Markdown format.

📌 **Usage:**
```python
api_key = "your-API-KEY"   # Replace with your Gemini API key
file_path = "/content/ast_code.py"  # Path to the code file
review_response = review_code_with_gemini(api_key, file_path)
print(review_response)
```

---

## 📊 **Sample Output**
The notebook outputs:
- Line-by-line code differences with highlights.
- Unbalanced bracket errors with line numbers.
- AI-generated code review feedback:
  - Syntax and logical issues.
  - Performance optimizations.
  - Best practices adherence.

---

## 📚 **Future Enhancements**
- 🛠️ Adding support for multiple programming languages.
- 🔥 Enhancing the diff viewer with a side-by-side comparison.
- 🌐 Improving API error handling and robustness.
- 🚀 Automating GitHub repository reviews with CI/CD integration.

---

## 💡 **Usage Tips**
- Customize the **Google Gemini API** prompt for more tailored feedback.
- Use **colorama** to make terminal output more readable.
- Adapt the **AST parsing** logic for multi-file analysis.

---

## 🛠️ **Installation Requirements**
To run this notebook locally, ensure you have:
- Python 3.7+
- Libraries: `colorama`, `requests`, `ast`, `IPython`

---

## 🌟 **Contributions**
Contributions and suggestions are welcome! Feel free to fork and enhance this AI-powered code review agent.

---

## 📄 **License**
This project is licensed under the MIT License. Feel free to use and modify it

✅ This README file covers:
- Installation steps
- Notebook features with usage examples
- Sample outputs
- Future improvements
- Contribution and license information

You can use it directly in your GitHub repository or Colab project. Let me know if you want any modifications or additional sections! 🚀
