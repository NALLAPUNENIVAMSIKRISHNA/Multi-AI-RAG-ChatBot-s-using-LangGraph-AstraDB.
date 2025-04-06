#  Hybrid Question Answering System using LangChain, Wikipedia & Cassandra

Colab Code Link :- https://colab.research.google.com/drive/1uTOney9ZHJTmKNT92mLYqPZ8MN7Bd0e2?usp=sharing

This project builds a **smart question-answering system** that chooses the best way to answer a user's question — either from a **vector database** of documents or from **Wikipedia** — using a decision-making **LLM agent**.

---

##  Purpose

To create a hybrid system that:
- Uses **pre-saved blog documents** (on AI, agents, LLMs) for specific queries.
- Uses **Wikipedia** for general knowledge.
- Automatically chooses the best source using an LLM.

---

## Tech Stack

- **LangChain & LangGraph** – to manage workflows and LLM calls.
- **Groq (Gemma LLM)** – routes the question to the right tool.
- **HuggingFace Embeddings** – convert text to vectors.
- **AstraDB (Cassandra)** – stores document vectors.
- **Wikipedia Tool** – answers general questions.

---

##  Flow

1. **User asks a question**
2. **LLM decides**:
   - If it's about AI/LLMs → search **vector store**
   - If general → search **Wikipedia**
3. **Fetches documents** based on decision
4. **Returns answer** to user

---

##  Example

- *“What is LangChain?”* → uses **vector DB** from AI blogs.
- *“Who is Virat Kohli?”* → uses **Wikipedia**.

---

##  Highlights

- Combines LLMs + document retrieval + web search
- Smart decision routing with Groq LLM
- Scalable vector store with AstraDB
- Simple yet powerful with LangGraph flow control
