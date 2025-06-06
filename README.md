# AI_MultiplePDF_Reader

AI_MultiplePDF_Reader is a Streamlit web application that allows you to upload multiple PDF files, process their content, and interactively ask questions about the combined content using Google's Gemini language model and vector search with FAISS.

## Features

- Upload and process multiple PDF files at once.
- Extracts and splits text from PDFs for efficient searching.
- Embeds text using Google Generative AI Embeddings.
- Stores and retrieves document embeddings using FAISS vector store.
- Asks questions in natural language and receives detailed answers based on      uploaded PDFs.
- User-friendly Streamlit interface.

## Requirements

- Python 
- Google API Key for Gemini (set in `.env` file)


## Installation

1. **Clone the repository:**
    
    git clone https://github.com/Sahil-Garg-01/AI_MultiplePDF_Reader.git
    cd AI_MultiplePDF_Reader
    
2. **requirements.txt**
    streamlit
    google-generativeai
    python-dotenv
    langchain
    PyPDF2
    chromadb
    faiss-cpu
    langchain_google_genai


3. **Install dependencies:**
    
    pip install -r requirements.txt
    

4. **Set up your environment variables:**
    - Create a `.env` file in the root directory.
    - Add your Google API key:
      
      GOOGLE_API_KEY=your_google_api_key_here
      

## Usage

1. **Run the Streamlit app:**
    
    streamlit run app.py
    

2. **In the web interface:**
    - Upload one or more PDF files using the sidebar.
    - Click "Submit & Process" to process the PDFs.
    - Ask questions about the content in the main input box.

## Project Structure

```
.
├── .env
├── .gitignore
├── app.py
├── README.md
├── requirements.txt
└── faiss_index/
    ├── index.faiss
    └── index.pkl
```

- `app.py`: Main Streamlit application.
- `faiss_index/`: Stores the FAISS vector index after processing PDFs.

## Notes

- Uploaded PDFs are processed in-memory; embeddings are stored locally in the `faiss_index/` directory.
- Make sure your Google API key has access to the Gemini model and embedding endpoints.

