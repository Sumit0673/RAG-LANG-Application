# Intelligent Document Query System

## Overview
This project enables users to create AI-driven chatbots for retrieving information from documents, books, or files using Retrieval-Augmented Generation (RAG). It leverages OpenAI's language model and vector databases to provide accurate, contextual responses based on user queries.

### Potential Applications
- Extract insights from large document collections.
- Build an interactive customer support chatbot.
- Automate knowledge retrieval for research and analysis.

## How It Works
1. **Data Processing**: Breaks down input documents into manageable text chunks (500–1000 words) for efficient retrieval.
2. **Vector Embeddings**: Converts text chunks into numerical representations and stores them in a Chroma vector database.
3. **Query Handling**: Matches user queries with relevant document chunks using similarity search.
4. **Response Generation**: Uses an OpenAI model to generate responses based on retrieved context.

## Setup Instructions
### 1. Clone the Repository
Run the following command in your terminal:
```sh
git clone https://github.com/Sumit0673/RAG-LANG-Application.git
```

### 2. Set Up OpenAI API Key
- Sign up at [OpenAI](https://platform.openai.com/api-keys) and generate an API key.
- Create a `.env` file in the project root and add:
```sh
OPENAI_API_KEY="your_secret_api_key"
```
- Add `.env` to `.gitignore` to prevent accidental commits.

### 3. Add Documents (Optional)
- Place text files inside the `data/` directory.
- Ensure `DATA_PATH` in `create_database.py` points to the correct directory.

### 4. Install Dependencies
Run:
```sh
pip install -r requirements.txt
```

### 5. Create the Vector Database
```sh
python create_database.py
```

### 6. Query the Database
Ask a question using:
```sh
python query_data.py "What are the supported operating systems for EC2?"
```

## Example Output
![Example Response](https://github.com/mlsmall/RAG-Application-with-LangChain/blob/main/output.png)

This setup allows for intelligent document querying using state-of-the-art NLP techniques.
