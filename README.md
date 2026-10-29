# HR Policy RAG System

This project is a Retrieval-Augmented Generation (RAG) system designed to answer questions based on an HR Policy Handbook. It uses LangChain, Google Gemini Embeddings, and the Groq LLM to retrieve relevant information from a PDF document and generate accurate, professional answers.

## Prerequisites

Before running this project, ensure you have Python installed on your system. We will use `uv`, an extremely fast Python package installer and environment manager, to set up the project. 

If you do not have `uv` installed, you can install it using pip:
```bash
pip install uv
```

## Setup Instructions

Follow these step-by-step instructions to run the project on your local machine.

### 1. Initialize the Project and Create a Virtual Environment

First, navigate to your project folder in the terminal. If you are starting fresh, you can initialize the project using `uv`:

```bash
uv init
```

Next, create a virtual environment to keep your project dependencies isolated:

```bash
uv venv
```

### 2. Activate the Virtual Environment

You need to activate the virtual environment before installing any packages.

* **For Windows:**
  ```bash
  .venv\Scripts\activate
  ```
* **For macOS and Linux:**
  ```bash
  source .venv/bin/activate
  ```

### 3. Install Dependencies

Once the virtual environment is activated, install all the required libraries using `uv`. If you have a `requirements.txt` file, run:

```bash
uv add -r requirements.txt
```

### 4. API Keys Configuration

This project requires API keys to access the embedding models and Large Language Models (LLMs). 

**Important Note:** I have already provided a `.env` file in this repository that includes my personal API keys so you can test the project immediately. However, if my API keys expire or reach their usage limit, the code might throw an error. In that case, you can easily use your own API keys. 

To use your own keys, open the `.env` file and replace the existing values with your own:

```env
GROQ_API_KEY="your_groq_api_key_here"
GOOGLE_API_KEY="your_google_api_key_here"
HUGGINGFACEHUB_API_TOKEN="your_huggingface_api_token_here"
```

### 5. Run the Project

Now that everything is set up, you can start the Jupyter Notebook to run the code:

```bash
jupyter notebook
```

Open the `HR_Policy_RAG_System.ipynb` file in your browser and run the cells one by one to see the RAG system in action!

## Note on Models

* **Embedding Model:** By default, the system uses Google Gemini (`gemini-embedding-2`). Instructions are provided inside the notebook to switch to HuggingFace if needed.
* **LLM:** By default, the system uses ChatGroq (`openai/gpt-oss-20b`). Instructions are provided inside the notebook to switch to Google Gemini if needed.
