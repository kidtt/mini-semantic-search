# Mini Semantic Search

## Overview

This project implements a semantic search system for Frequently Asked Questions (FAQs) using Python, Pandas, Sentence Transformers, and ChromaDB.

Unlike keyword-based search, semantic search uses text embeddings to retrieve content based on meaning.

## Features

* Loads FAQ data from CSV using Pandas.
* Cleans missing values, whitespace, and duplicate questions.
* Chunks FAQ question-answer pairs.
* Generates embeddings using `all-MiniLM-L6-v2`.
* Stores embeddings in ChromaDB.
* Retrieves and displays the top three matching FAQs.

## Project Structure

```text
mini-semantic-search/
├── data/
│   └── faqs.csv
├── notebooks/
│   └── semantic_search.ipynb
├── chroma_db/
├── README.md
└── requirements.txt
```

## Installation

Create and activate a virtual environment, then install the dependencies:

```bash
python -m venv .venv
```

On Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

Open `notebooks/semantic_search.ipynb` in VS Code and select the `.venv` Python kernel.

## Example Queries

* I forgot my password and cannot log in.
* How do I contact customer service?
* I want to delete my account.
* Where can I find my delivery information?

## Technologies

* Python
* Pandas
* Sentence Transformers
* ChromaDB
* Jupyter Notebook

## How It Works

1. Load FAQ data from CSV.
2. Clean and prepare the data.
3. Create one text chunk per FAQ.
4. Generate embeddings for each chunk.
5. Store embeddings and documents in ChromaDB.
6. Embed a search query and retrieve the three most similar FAQs.

## Limitations

Results depend on the quality of the FAQ data and the embedding model. Semantic similarity does not guarantee that every retrieved answer is correct.
