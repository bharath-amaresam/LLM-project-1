# 🧠 AtliQ Tees: Talk to a Database (GenAI Project)

## 🚀 Project Overview

**AtliQ Tees** is a fashion-forward T-shirt brand managing inventory, sales, and discounts in a MySQL database. Store managers regularly seek insights like:

    > “How many black Nike t-shirts are in stock?”  
    > “What revenue can we expect if we sell all small-size Adidas tees after discounts?”

Traditionally, these questions required SQL skills. But with this **GenAI-powered solution**, store managers can ask in **plain English** and get instant, data-backed answers.

---

## 🧬 Why GenAI?

Generative AI (GenAI) has evolved far beyond rule-based bots. Today’s LLMs **understand context**, **reason like humans**, and **generate accurate SQL queries** from natural language prompts.

In this project, GenAI acts like your **data-savvy assistant**—fluent in SQL, schema-aware, and ready to answer any business question.

---

## 🧠 Core Components of the Project

### 1. 🧠 LLM (Large Language Model)
We use [**Hugging Face Transformers**](https://huggingface.co/models) with powerful instruction-tuned models such as:

- [`mistralai/Mistral-7B-Instruct`](https://huggingface.co/mistralai/Mistral-7B-Instruct)
- [`google/flan-t5-xxl`](https://huggingface.co/google/flan-t5-xxl)
- (Optionally) OpenAI GPT-4 if available via API

These LLMs are used to convert natural questions into structured SQL queries.

---

### 2. 🧭 Embeddings & Vector Database (ChromaDB)

To understand fuzzy or abstract queries like:

> “What if we sell out all breathable summer-friendly tees?”

...we apply **semantic search** using embeddings.

- Product descriptions, metadata, and database schema are converted into **dense vector embeddings** using **Hugging Face Sentence Transformers** (e.g., `all-MiniLM-L6-v2`).
- These vectors are stored in **[ChromaDB](https://www.trychroma.com/)**, a fast and lightweight vector database.

When a question is asked, its vector is compared to stored embeddings to retrieve **relevant context**.

---

### 3. 📚 RAG: Retrieval-Augmented Generation

LLMs don’t know your live database content. So we use **RAG** to improve accuracy:

- **Retrieve** the relevant schema or product-related information from ChromaDB.
- **Augment** the LLM prompt with this contextual data.
- **Generate** SQL and answers more accurately.

This bridges the gap between pretrained LLMs and your private data.

---

### 4. 🔗 LangChain: The Workflow Engine

We use [**LangChain**](https://www.langchain.com/) to orchestrate the full workflow:

- Understand the user prompt
- Pull relevant context using ChromaDB
- Construct a dynamic prompt for the LLM
- Get SQL from the LLM
- Run the query on **MySQL**
- Return results as a human-readable answer

LangChain makes it easy to **chain together retrieval, generation, and execution** logic.

---

### 5. 🎛️ UI Layer (Streamlit)

A lightweight and interactive front-end is built using [**Streamlit**](https://streamlit.io/). Store managers simply type (or soon, speak) their question—no SQL needed!

---

## 🧱 Tech Stack Summary

| Component        | Technology Used                                |
|------------------|-------------------------------------------------|
| 💬 LLM           | Hugging Face (Mistral-7B, FLAN-T5) or OpenAI GPT |
| 🧠 Embeddings    | Hugging Face Sentence Transformers (`MiniLM`)   |
| 📦 Vector DB     | ChromaDB                                        |
| 🧠 Orchestration | LangChain                                       |
| 💻 UI            | Streamlit                                       |
| 🗃️ Database      | MySQL                                           |

---

## 📚 Learning Outcomes

- How LLMs can generate SQL from plain English
- Role of **embeddings** in semantic search
- How **RAG** improves GenAI accuracy with private data
- LangChain’s role in chaining logic
- Building **natural language interfaces** for databases

---

## 📈 Sample Query Example

**User Input**  
> “How much sales amount will be generated if we sell all small-size Adidas t-shirts today after discounts?”

**Output**  
> `3165` (as computed from MySQL after SQL generation & execution)

---

## 🔮 Future Enhancements

- 🎙️ **Voice queries** via speech-to-text integration
- 📊 **Chart-based results** for trend insights
- 🔁 **LangGraph** integration for advanced workflows (looping, conditional prompts)
- 🔐 Add authentication for secure data access

## **credits**
- This project is part of code basics [GenAI course](https://www.youtube.com/watch?v=d4yCWBGFCEs&t=125s)
- Big thanks to **Dhaval Patel Sir** for this tutitoral 
- [github repo](https://github.com/codebasics/langchain/tree/main/4_sqldb_tshirts)

<br>
<br>
<br>

# Hi, I'm Bharath! 👋

## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://codebasics.io/portfolio/Amaresam-Sai-Bharath-Chand)
&emsp;
[![Gmail](https://img.shields.io/badge/bharath.temp3@gmail.com-white?logo=Gmail)](mailto:bharath.temp3@gmail.com)
&emsp;
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/amaresam-sai-bharath-chand-47ba50168/)
&emsp;
[![youtube](https://img.shields.io/badge/youtube-1DA1F2?style=for-the-badge&logo=youtube&logoColor=red)](https://youtu.be/ZkzLYNFPqwk)
&emsp;
