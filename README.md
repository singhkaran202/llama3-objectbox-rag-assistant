# Llama3 ObjectBox RAG Assistant

A Streamlit application that uses ObjectBox as a vector database and Llama3-8b model via Groq to answer questions about documents using Retrieval Augmented Generation (RAG).

## Features

- **Document Processing**: Process PDF documents for analysis and question-answering
- **ObjectBox Vector Database**: Efficient vector storage and retrieval using ObjectBox
- **Retrieval-Augmented Generation**: Combines Llama3's reasoning with contextual document retrieval
- **OpenAI Embeddings**: Creates high-quality vector representations of document chunks
- **Interactive UI**: Clean Streamlit interface with expandable context view

## Tech Stack

- **LLM**: Llama3-8b-8192 via Groq API
- **Embeddings**: OpenAI Embeddings
- **Vector Store**: ObjectBox for persistent and efficient vector storage
- **Document Processing**: LangChain's document loaders and text splitters
- **Frontend**: Streamlit

## Setup

### Prerequisites

- Python 3.8+
- Groq API key
- OpenAI API key
- ObjectBox installed on your system

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/llama3-objectbox-rag-assistant.git
cd llama3-objectbox-rag-assistant
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Create a `.env` file in the project root with your API keys
```
GROQ_API_KEY=your_groq_api_key
OPENAI_API_KEY=your_openai_api_key
```

4. Create a directory for your PDFs
```bash
mkdir us_census
```

5. Add your PDF files to the `us_census` directory

### Running the App

```bash
streamlit run app.py
```

## Usage

1. Launch the application
2. Click "Documents Embedding" button to process documents and create the ObjectBox vector database
3. Enter your question about the documents in the text input
4. View the AI-generated answer based on the document content
5. Expand "Document Similarity Search" to see the relevant document chunks used for the response

## Implementation Details

- Uses OpenAI embeddings with 768 dimensions for document representation
- Document chunking with 1000 characters per chunk and 200 character overlap
- Persistent storage of vectors using ObjectBox database
- Response time tracking for performance monitoring

## Benefits of ObjectBox

- Persistent storage of vector embeddings
- Fast similarity search capabilities
- Lower memory footprint compared to in-memory solutions like FAISS
- Better scalability for larger document collections

## Future Improvements

- Add support for more document formats
- Implement streaming responses
- Add document upload through the Streamlit UI
- Implement conversation history for follow-up questions
- Add metadata filtering options
