
# Generative AI with LangChains — Environment Setup Guide

Welcome to the **Generative AI with LangChain Series**! This repository contains all the Jupyter notebooks, code examples, and supporting resources needed to follow along with our medium blog series on building Generative AI applications using LangChain.

This guide will help you set up a Python environment that works seamlessly with **Jupyter Notebooks** inside **Visual Studio Code (VS Code)**. This setup ensures a consistent and isolated development environment, making it easier to experiment with LLMs, agents, RAG, and more.

---

## Folder Structure

All notebooks are organized chapter-wise under the `notebooks/` directory. Each chapter aligns with a specific blog post and builds progressively on the concepts covered earlier.


---

## Environment Setup for LangChain Tutorials (Jupyter + VS Code)

This guide will help you set up a Python environment for running LangChain tutorials in **Jupyter Notebooks** and connect it as a kernel in **Visual Studio Code**.

---

### Step 1: Clone the Repository

```bash
git clone https://github.com/piyushagni5/langchain-ai.git
cd langchain-ai
```

---

### Step 2: Create and Activate a Virtual Environment

Using **`venv`**:

```bash
python -m venv .venv
# Activate it
# For macOS/Linux
source .venv/bin/activate
# For Windows
.venv\Scripts\activate
```

Or using **`conda`**:

```bash
conda create -n langchain-env python=3.10 -y
conda activate langchain-env
conda install pip
```

---

### Step 3: Install Required Dependencies

Install core dependencies:

```bash
pip install --upgrade pip
pip install -r requirement.txt
```

---

### Step 4: Add Environment as a Jupyter Kernel

Install the Jupyter kernel package:

```bash
pip install ipykernel
```

Register your environment as a Jupyter kernel:

```bash
python -m ipykernel install --user --name=langchain-env --display-name "LangChain (env)"
```

---

### ✅ Step 5: Open in VS Code and Select Kernel

1. Launch **VS Code** and open this project folder.
2. Open any `.ipynb` notebook.
3. From the top-right **kernel selector**, choose:

   ```
   LangChain (env)
   ```
4. You’re all set to start running LangChain notebooks in VS Code!

---
### Step 6: Set Up API Keys
To implement the code we will require external LLM providers like OpenAI, Google Gemini, or Hugging Face.

1. Create a .env file in the project root:

```bash
touch .env
```

2. Add the following to `.env`:

```
OPENAI_API_KEY=your_openai_key
GOOGLE_API_KEY=your_google_generativeai_key
HUGGINGFACEHUB_API_TOKEN=your_huggingface_token
```

3. Load them in your Python code:

```python
from dotenv import load_dotenv
load_dotenv()
```

> Only include keys relevant to the provider you're using in that notebook.





### Step 6 (Optional): Jupyter Notebook Extensions

To improve your Jupyter experience, you can install:

```bash
pip install jupyter_contrib_nbextensions
jupyter contrib nbextension install --user
```

---

### 🔁 Updating Requirements

If you install more packages later:

```bash
pip freeze > requirements.txt
```

To install everything from scratch next time:

```bash
pip install -r requirements.txt
```

---
