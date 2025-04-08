# 💬 RAG Chat with Document using ChromaDB and OpenAI

This project demonstrates a **Retrieval-Augmented Generation (RAG)** pipeline using **ChromaDB** as a vector database and **OpenAI’s GPT-3.5 Turbo** for answering questions based on custom text documents (such as news articles). It loads, chunks, embeds, and indexes the data locally — then allows for real-time querying.

---

## 📂 Project Structure

```bash
rag_chat_with_doc/
│
├── .env                      # Your OpenAI API key should be stored here
├── chroma_persistent_storage/ # ChromaDB vector store (generated at runtime)
├── news_articles/            # Folder containing .txt files used as knowledge base
├── main.py                   # Main script for RAG pipeline
└── README.md                 # Project documentation
```


## ⚙️ Features

  - ✅ Load `.txt` documents from a directory  
  - ✅ Split documents into manageable chunks  
  - ✅ Generate embeddings using `text-embedding-3-small` model from OpenAI  
  - ✅ Store embeddings in a **persistent** ChromaDB collection  
  - ✅ Retrieve top-n relevant chunks using semantic search  
  - ✅ Generate concise and contextual answers using **GPT-3.5-Turbo**



## 🔧 Installation


### 1. Clone the repository

```bash
git clone https://github.com/SushilkumarBarai/rag_chat_with_doc.git
cd rag_chat_with_doc
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```


### 3. Sample requirements.txt content:

```bash
openai
chromadb
python-dotenv
```

### 4. Add your OpenAI API key

```bash
OPENAI_API_KEY=your_openai_key_here
```

### 5. Run the main script

```bash
python main.py
```


### 6. Example usage

```bash
question = "tell me about venture capital"
relevant_chunks = query_documents(question)
answer = generate_response(question, relevant_chunks)
print(answer)
```


---

## 💼 Use Case

This project is ideal for:

- **Internal knowledge base querying**: Upload documents like product manuals, support articles, or company policies and let the bot answer user queries.
- **Customer support automation**: Provide precise and contextual answers based on support documentation.
- **Educational tools**: Help students find relevant answers from academic texts or research papers.
- **Legal or compliance teams**: Search legal documents or policy guidelines using natural language.
- **News summarization & QnA**: Ingest news articles and ask questions to get concise summaries or factual insights.

---

## 🧾 Conclusion

The `rag_chat_with_doc` project demonstrates the power of combining **embedding-based search** with **language generation** for intelligent document querying. By integrating OpenAI's API with ChromaDB, it enables fast and accurate retrieval of relevant context and generates human-like answers. This approach can significantly enhance productivity in research, customer service, and data exploration workflows.

Feel free to extend the project with PDF ingestion, UI integration, or support for multilingual documents!
