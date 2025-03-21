# LangChain RAG with LLAMA3

## Overview
This repository implements Retriever-Augmented Generation (RAG) using LangChain and LLAMA3 model. The purpose of this project is to enhance responses by generative AI by using retreival-based techniques in large language models (LLMs). This approach allows models to output real-time information from external sources that are not part of the model's training datasets, which makes the responses more accurate and relevant. 

## Features
- **WebBaseLoader**: Retrieves and loads articles written at any point in time into the code
- **RecursiveCharacterTextSplitter**: Splits the text inside the article/document into chunks
- **HuggingFaceEmbeddings** with **sentence-transformers/all-mpnet-base-v2**: Converts text into vector embeddings
- **FAISS Vector Database**: Stores vector embeddings in a database for efficient searching and retrieval
- **ConversationalRetrievalChain**: Uses relevant documents to generate responses to the user using **LLAMA3 via Ollama**

## How it Works
1. Loads the web document by inserting the URL into the code.
2. Splits the document into smaller, manageable chunks for embedding
3. Converts text in the document into vector embeddings and stores them in FAISS
4. Uses LLAMA3 to generate responses based on context given by the user
5. Keeps the chat history for any follow up questions

## Dependencies
- Python 3.8+
- LangChain
- FAISS
- LLAMA3 via Ollama API
- Sentence-Transformers
- BeautifulSoup (bs4)
- Replicate API

## Example Query
```python
question = "What's new with Llama 3?"
result = chat_chain({"question": question, "chat_history": chat_history})
print(result['answer'])
```

## Contact
For questions, reach out to **Poojitha Kommera** at poojithakommera@gmail.com.
