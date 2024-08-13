
# RAG Document Question Answer

This project implements a Retrieval-Augmented Generation (RAG) system for answering questions based on a given document. The system uses a combination of a vector database and generative AI to provide accurate responses to queries by retrieving relevant information from a document and generating a comprehensive answer.

## Features

- **Document Ingestion**: Upload a document that the system will use to build a knowledge base.
- **Question Answering**: Ask questions related to the ingested document, and the system will retrieve the most relevant information and generate an answer.
- **Local Deployment**: Run the entire system locally with the help of Docker and an NVIDIA GPU for acceleration.

## Setup

### Prerequisites

- Docker
- Python 3.8+

### Environment Variables

The project requires certain environment variables to be set, which are defined in the `.env` file. An example `.env` file is provided. You need to copy this file and update the values accordingly.

```bash
cp .env.example .env
```

### Install Dependencies

Create a virtual environment and install the necessary dependencies:

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Run the Notebook

To run the system, simply open the Jupyter Notebook:

```bash
jupyter notebook rag_document_question_answer.ipynb
```

### Qdrant running in Docker

Run your qdrant vector data store using docker:

```bash
docker run -d --name qdrant -p 6333:6333 qdrant/qdrant
```

This will expose the qdrant datastore on `http://localhost:6333/dashboard#/collections`.
