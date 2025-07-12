**📘 Retrieval-Augmented Question Answering with Gemini training from @MarkTechStation**
This project implements a simple Retrieval-Augmented Generation (RAG) pipeline that allows users to ask natural language questions and receive context-based answers powered by Google's Gemini large language model.

**🔧 Features**
📄 Document Splitting: Load a Markdown file and split it into meaningful chunks.
🧠 Text Embedding: Use text2vec-base model to convert each chunk into a numerical vector.
🗃️ Vector Storage: Store vectors in an in-memory ChromaDB collection.
🔍 Semantic Search: Given a user question, retrieve the most relevant chunks using vector similarity.
🎯 Re-ranking: Improve relevance by re-ranking retrieved chunks with a cross-encoder model.
✨ Answer Generation: Feed the top-ranked chunks into Gemini to generate accurate, grounded responses.

**📦 Dependencies**
Install the required libraries with:   pip install -r requirements.txt

**Typical dependencies include:**
sentence-transformers
chromadb
google-generativeai
python-dotenv


**🚀 How It Works**
Preprocessing: Split doc.md into smaller paragraphs.
Embedding: Convert each paragraph into a vector.
Store: Save those vectors in ChromaDB with unique IDs.
Query: Embed the user's question and retrieve top-K similar chunks.
Re-rank: Use a cross-encoder to improve result quality.
Generate: Use Gemini to answer the question based only on the retrieved chunks.

📁 **Environment**
Make sure you set your Gemini API key in a .env file:
GOOGLE_API_KEY=your_gemini_api_key_here
