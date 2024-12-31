# README.md
# Azure OpenAI Assistant RAG API

This project implements a Retrieval Augmented Generation (RAG) system using Azure OpenAI Assistants.

## Setup Instructions

1. Clone the repository:
```bash
git clone [your-repo-url]
cd azure_rag_assistant
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Create .env file:
```bash
cp .env.example .env
```

5. Update .env with your Azure OpenAI credentials:
```
AZURE_OPENAI_API_KEY=your_api_key_here
AZURE_OPENAI_ENDPOINT=your_endpoint_here
AZURE_OPENAI_DEPLOYMENT_NAME=your_deployment_name_here
```

6. Run the application:
```bash
uvicorn app.main:app --reload
```

The API will be available at http://localhost:8000

## API Endpoints

1. POST /upload/
   - Upload PDF documents
   - Request: Multipart form data with PDF files

2. POST /query/
   - Query the documents
   - Request body: {"question": "your question here"}

3. GET /status/
   - Get system status

## API Documentation
- Swagger UI: http://localhost:8000/docs
- ReDoc: http://localhost:8000/redoc
