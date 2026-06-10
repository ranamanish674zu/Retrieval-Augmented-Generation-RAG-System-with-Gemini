
```markdown
# Retrieval Augmented Generation (RAG) System with Gemini

This repository contains a Google Colab notebook demonstrating a basic Retrieval Augmented Generation (RAG) system using FAISS for efficient document retrieval, Sentence Transformers for text embeddings, and the Google Gemini API for natural language generation.

## Project Overview

Retrieval Augmented Generation (RAG) combines the strengths of information retrieval with the power of large language models (LLMs). This project showcases how to:

1.  **Embed Documents**: Convert a collection of text documents into numerical vector representations (embeddings) using a pre-trained Sentence Transformer model.
2.  **Index Embeddings**: Store and efficiently search these embeddings using FAISS (Facebook AI Similarity Search) for fast similarity lookups.
3.  **Retrieve Relevant Context**: Given a user query, find the most relevant documents from the indexed collection.
4.  **Augment and Generate**: Pass the retrieved relevant documents as context to a Google Gemini model, along with the original query, to generate a more informed and accurate response.

## Features

*   **Sentence Transformers**: Used for generating high-quality embeddings.
*   **FAISS**: An efficient library for similarity search on large datasets of vectors.
*   **Google Gemini API**: Utilized for generating augmented responses based on retrieved context.
*   **Modular Design**: Clear separation of components for embeddings, indexing, retrieval, and generation.

## Setup and Installation

1.  **Open in Google Colab**: Click the "Open in Colab" badge above (if available) or simply open the `.ipynb` file in Google Colab.

2.  **Install Dependencies**: Run the first code cell in the notebook to install the required libraries:

    ```python
    !pip install faiss-cpu sentence-transformers google-generativeai
    ```

3.  **Google Gemini API Key**: 
    *   Obtain a Google Gemini API key from [Google AI Studio](https://aistudio.google.com/app/apikey).
    *   In Google Colab, go to the left-hand panel, click on the "🔑 Secrets" icon.
    *   Add a new secret named `GOOGLE_API_KEY` and paste your Gemini API key as its value.

4.  **Run the Notebook**: Execute all cells sequentially. The notebook will:
    *   Define sample documents.
    *   Create embeddings and a FAISS index.
    *   Perform a similarity search to retrieve relevant documents.
    *   Use the retrieved context and your query to generate a response with the Gemini API.

## Usage

Modify the `documents` list and the `query` variable in the respective cells to experiment with your own data and questions.

```python
# Example query
query = "What is RAG? Explain in 200 words?"
```

## Technologies Used

*   Python
*   Google Colab
*   `sentence-transformers`
*   `faiss-cpu`
*   `google-generativeai`

```
