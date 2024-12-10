# University Admission FAQ Chatbot

This project is a **university-focused Retrieval-Augmented Generation (RAG) chatbot** designed to assist prospective students and applicants by answering frequently asked questions about admissions. Built with **LangChain**, **Streamlit**, and other APIs, the chatbot offers a conversational interface for users to retrieve precise and contextual information directly from reliable sources.

---

## Features

- **AI-Powered Responses**: Utilizes LangChain's integration with advanced language models (e.g., LLaMA2) for accurate and relevant answers.
- **Retrieval-Augmented Generation (RAG)**: Combines embedding-based document retrieval with LLM responses for context-aware answers.
- **Multi-document Search**: Parses and indexes content from multiple web pages (e.g., FAQ sections of admissions websites).
- **Interactive Web UI**: A Streamlit-based interface allowing users to input queries and receive responses in real time.
- **Efficient Text Splitting**: Breaks down large documents into manageable chunks for better embeddings and retrieval accuracy.

---

## How It Works

1. **Document Loading**:
   - The bot loads FAQ pages using LangChain's `WebBaseLoader`.
   - Extracted content is parsed with BeautifulSoup to focus on relevant sections (e.g., headers, FAQ answers).

2. **Text Processing**:
   - Extracted documents are split into chunks using LangChain's `RecursiveCharacterTextSplitter` for optimized embeddings.

3. **Vector Database**:
   - Uses `FAISS` to store document embeddings, enabling efficient similarity search for user queries.

4. **RAG Pipeline**:
   - Combines a retriever with a language model using LangChain's `create_retrieval_chain` for context-based responses.

5. **Interactive Query**:
   - Users interact with the chatbot via a simple Streamlit UI, inputting queries to receive immediate, AI-generated answers.

---

## Getting Started

### Prerequisites

- Python 3.8+
- Required Libraries: `streamlit`, `langchain`, `faiss`, `bs4`, `dotenv`, `nomic`

### Setup Instructions

1. Clone the repository:
   ```bash
   git clone <repo_url>
   cd <repo_directory>
