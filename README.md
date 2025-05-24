# Graph-RAG with Neo4j, LangChain, and Groq LLM

This project shows how to build a **graph-based Retrieval-Augmented Generation (RAG)** system using a **Neo4j graph database**, **LangChain**, and **Groq’s LLM**.

## What It Does

The notebook:

* Connects to a Neo4j graph database
* Loads and stores knowledge (e.g., Elon Musk’s bio and a movie dataset)
* Uses a **Graph Transformer** to extract entities and relationships from text
* Builds a graph from text and CSV data
* Queries the graph using Cypher
* Integrates an LLM to answer questions based on graph content

---

## Notebook: `graph_rag.ipynb`

### Key Steps:

1. **Install Packages**
   Uses `langchain`, `langchain-community`, `neo4j`, `langchain-groq`, and `langchain-experimental`.

2. **Connect to Neo4j**
   Set environment variables for URI, username, and password to connect.

3. **Load LLM**
   Uses Groq’s `Gemma2-9b-It` model via API key.

4. **Ingest Text Data**
   Elon Musk’s bio is converted into `Document` format for processing.

5. **Extract Graph from Text**
   `LLMGraphTransformer` is used to extract nodes and relationships.

6. **Load Movie Dataset**
   Loads a CSV of movies with metadata (titles, directors, actors, genres) into Neo4j using Cypher.

---

## Requirements

Install with:

```bash
pip install langchain langchain-community langchain-groq langchain-experimental neo4j
```

---

## Concepts Used

* **LLMGraphTransformer** – turns unstructured text into a graph format
* **Neo4j + Cypher** – used for graph storage and queries
* **LangChain + Groq** – powers the language model’s generation
* **Graph-RAG** – LLM fetches graph context before generating output

---

## How to Run

1. Open the notebook in Jupyter or Google Colab
2. Replace Neo4j and Groq credentials with your own
3. Run all cells to build and query the graph

---


![image](https://github.com/user-attachments/assets/206ab6a0-0d81-4550-acbf-5818f6b15fd0)
![image](https://github.com/user-attachments/assets/71e4628d-20a4-4fee-aa80-700feeffa815)

