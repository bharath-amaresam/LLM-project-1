# 🧠 AtliQ Tees: Talk to a Database (GenAI Project Overview)

## 🚀 Introduction
AtliQ Tees is a fashion-forward t-shirt brand that manages its operations—sales, inventory, and discounts—in a structured MySQL database. Store managers often need answers like:

    “How many black Nike t-shirts are in stock?”
    “What revenue can we expect if we sell all small-size Adidas tees after applying discounts?”

Traditionally, these questions required SQL knowledge. But in our GenAI-powered system, managers can ask natural language questions—and get instant, data-backed answers.

## 🧬 Why GenAI?
Generative AI (GenAI) has evolved from static chatbot scripts to intelligent systems that understand context, reason like a human, and generate SQL, summaries, and insights.

🌟 In our project, GenAI acts like a data-savvy sales analyst who's read the entire product catalog and understands your every question.

## 🧠 Core Components of the Project
### 1. LLM (Large Language Model) <br/>
We use Google PaLM API, a powerful LLM trained on billions of language patterns.

### 2. Embeddings & Vector Database (ChromaDB)<br/>
Understanding the intent behind a question like:

       “What if we sell out all breathable summer-friendly tees?”

...requires semantic understanding. So we:

- Convert each product description + schema info into embeddings using Hugging Face models.
 
- Store them in ChromaDB, a vector database.

When a query is made, we compare its embedding to the database to fetch the most relevant context.

### 3. RAG: Retrieval-Augmented Generation
LLMs don’t know everything. Especially not your latest inventory. So we use RAG:

- Retrieve relevant schema and product data from vector DB

- Feed that to the LLM for better context

- Generate highly accurate SQL and answers


### 4. LangChain: The Brain Behind the Workflow
LangChain orchestrates every step:

- Breaks down the prompt

- Retrieves schema/data context

- Sends everything to the LLM

- Executes the SQL query

- Returns the result

### 5. UI Layer (Built with Streamlit)
Used Streamlit to build a clean front-end for store managers.

## 🧱 Tech Stack Summary

- LLM  :	Google PaLM API
- Embeddings : Hugging Face Sentence Transformers
- Vector DB : ChromaDB
- Orchestration : LangChain
- UI	: Streamlit
- Database: MySQL

## 📚 Learning Outcomes
- The role of LLMs in generating SQL
- The power of embeddings and vector search
- How RAG ensures better accuracy in GenAI apps
- LangChain's orchestration capabilities
- How to build natural language database interfaces

### 📦 Future Enhancements
- Enable voice queries using speech-to-text
- Add chart-based answers (e.g., revenue trends)
- Integrate with LangGraph for more complex workflows

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
