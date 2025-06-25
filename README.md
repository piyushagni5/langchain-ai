
# Generative AI with LangChains — Environment Setup Guide

Welcome to the **Generative AI with LangChain Series**! This repository contains all the Jupyter notebooks, code examples, and supporting resources needed to follow along with our medium blog series on building Generative AI applications using LangChain.

This guide will help you set up a Python environment that works seamlessly with **Jupyter Notebooks** inside **Visual Studio Code (VS Code)**. This setup ensures a consistent and isolated development environment, making it easier to experiment with LLMs, agents, RAG, and more.

## 📚 Posts in this Series: Generative AI Using LangChain

### 🔹 Part 1: The LangChain Fundamentals
- **1.1** [Introduction to LangChain](https://medium.com/@piyushagni5/generative-ai-with-langchain-introduction-part-1-881a872a7644)  
- **1.2** Models: The Brains of Your AI Application  
- **1.3** Prompt Engineering 
- **1.4** Structured Output & Output Parsers  
- **1.5** Building Chains in LangChain  
- **1.6** Memory: Giving LLMs a Long-Term Recall  

### 🔹 Part 2: Enhancing LLMs with External Data
- **2.1** Document Loaders and Text Splitters  
- **2.2** Embeddings: Understanding Text Semantics  
- **2.3** Vector Databases and Similarity Search  

### 🔹 Part 3: Advanced LangChain Applications
- **3.1** Agents: Empowering LLMs with Decision-Making  
- **3.2** Retrieval-Augmented Generation (RAG)  
- **3.3** Debugging & Testing with LangSmith  

### 🔹 Part 4: Real-World Use Cases
- **4.1** Building a Chatbot with LangChain
---

## Folder Structure

All notebooks are organized chapter-wise. Each chapter aligns with a specific blog post and builds progressively on the concepts covered earlier.


---

## Environment Setup for LangChain Tutorials (Jupyter Notebook + VS Code)

This guide will help you set up a Python environment for running LangChain tutorials in **Jupyter Notebooks** and connect it as a kernel in **Visual Studio Code**.


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

### Step 5: Open in VS Code and Select Kernel

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
ANTHROPIC_API_KEY
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
