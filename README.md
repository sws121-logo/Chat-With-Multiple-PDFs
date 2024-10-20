# Chat-With-Multiple-PDFs
Here’s a professional `README.md` for your Streamlit app that enables users to chat with multiple PDFs using LangChain, OpenAI, and FAISS:

```markdown
# PDF Conversational AI with LangChain

## Goal of the Project

The goal of this project is to build an interactive Streamlit web application where users can upload multiple PDF files and ask questions about the content. The application processes the PDFs, splits the text into manageable chunks, and utilizes embeddings to create a vector store for efficient conversational retrieval. The system answers user queries by retrieving relevant content from the uploaded PDFs.

## Purpose of the Project

This project aims to:
- Enable users to interact with and retrieve information from large PDF documents.
- Provide an intuitive chat interface where users can query multiple PDFs simultaneously.
- Leverage AI-based language models (such as OpenAI or HuggingFace models) for document understanding and answering user questions.
- Efficiently process large chunks of text and return precise responses through a conversational interface.

---

## Overview

This application uses the following technologies:
- **Streamlit**: For building the user interface and chat interaction.
- **LangChain**: To manage text splitting, embeddings, vector storage, and retrieval chains.
- **FAISS**: For efficient vector-based retrieval of document chunks.
- **OpenAI / HuggingFace**: As the language model provider for generating conversational responses.

Users can upload PDF documents, and the app will extract text, split it into chunks, and generate vector embeddings for search and retrieval. The chat interface allows users to ask questions about the documents, with responses generated by an AI language model.

---

## Technology Stack

- **Streamlit**: Web framework for building the interactive app.
- **LangChain**: Library for managing text and language models.
- **FAISS**: Vector store for efficient document chunk retrieval.
- **OpenAI or HuggingFace models**: Language models to handle conversational queries.
- **PyPDF2**: For PDF text extraction.

---

## Installation and Setup

To run this project locally, follow the steps below:

### Prerequisites

- **Python 3.7+**
- **pip** (Python package manager)
- **OpenAI API Key** (If using OpenAI as the language model)

### Steps to Run:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/pdf-conversational-ai.git
   cd pdf-conversational-ai
   ```

2. **Install Dependencies**:
   Install the required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up Environment Variables**:
   Create a `.env` file in the root directory with the following content:
   ```bash
   OPENAI_API_KEY=your-openai-api-key
   ```

4. **Run the Application**:
   Start the Streamlit application:
   ```bash
   streamlit run app.py
   ```

5. **Access the Application**:
   Open the web browser and navigate to `http://localhost:8501` to interact with the app.

---

## How It Works

1. **Upload PDFs**: Users can upload multiple PDF files from the sidebar.
2. **Process PDFs**: The app extracts text from the uploaded PDFs and splits the text into manageable chunks.
3. **Create Vector Store**: The text chunks are transformed into vector embeddings using either OpenAI or HuggingFace models.
4. **Conversational Interaction**: Users can ask questions about the PDFs in a chat interface. The app retrieves relevant chunks and generates responses using an AI language model.

### Key Components:

- **PDF Text Extraction**: Extracts raw text from the uploaded PDFs using `PyPDF2`.
- **Text Chunking**: Splits the extracted text into smaller chunks for better processing.
- **Vector Store**: Creates a FAISS-based vector store from the text chunks using embeddings.
- **Conversational Chain**: Uses LangChain’s `ConversationalRetrievalChain` to handle the chat interaction with context.

---

## Project Structure

```bash
.
├── app.py                 # Main Streamlit application
├── htmlTemplates.py        # HTML templates for styling chat messages
├── requirements.txt        # Required Python libraries
├── .env                    # Environment variables
└── utils/
    ├── Store.py            # Placeholder for additional utilities
    ├── ...                 # Other helper files
```

### Example Flow:

1. **Upload PDFs**: Use the sidebar to upload one or more PDF documents.
2. **Process PDFs**: Click the 'Process' button to extract and process the PDF text.
3. **Ask Questions**: Input your query in the text box and receive relevant answers from the PDFs based on your question.

---

## Future Enhancements

- **Real-time Embeddings Update**: Allow users to add more PDFs after the initial processing without reprocessing the entire set.
- **Real-time Conversations**: Improve response speed by pre-processing the PDFs and using an optimized retrieval model.
- **Enhanced PDF Parsing**: Implement better handling for PDFs with complex layouts (e.g., tables, images).
- **Support for More Formats**: Expand the application to support additional document formats such as Word or HTML.

---

## License

This project is licensed under the MIT License. Feel free to use and modify it for your own projects.
```

