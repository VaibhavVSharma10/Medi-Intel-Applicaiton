# Medi-Intel-Applicaiton
MediMind Bot is a medical data extraction and analysis tool designed to reduce hallucination and enhance performance. It utilizes BioMistral and PubmedBERT for data extraction and a self-hosted Qdrant database on Docker for scalable analysis. The bot is designed to process data from 3 documents in under a minute and provide accurate insights with minimal errors.

    1. Created a medical bot with reduced hallucination, extracting data from 3 documents in under a minute using BioMistral and PubmedBERT.
    2. Engineered a scalable RAG application with minimal hallucination using a self-hosted Qdrant database on Docker.
    3. Implemented FAST API for streamlined result retrieval, significantly reducing response times and improving accessibility.

Possible Use Cases:

  Medical Research: Researchers can use MediMind Bot to extract and analyze data from medical journals and publications, facilitating research in various medical fields.

  Clinical Decision Support: Healthcare professionals can leverage the bot's insights to make informed clinical decisions and provide personalized patient care.
  
  Drug Discovery: Pharmaceutical companies can use the bot to analyze drug-related data and identify potential candidates for drug discovery and development.
  
  Healthcare Analytics: Hospitals and healthcare organizations can use the bot to analyze patient data, trends, and outcomes to improve healthcare delivery and patient outcomes.


How to Run

Command 1

Pull the Qdrant Docker image:

    docker pull qdrant/qdrant

Command 2

Run the Qdrant Docker container with port mapping and volume mounting:

    docker run -p 6333:6333 -p 6334:6334 -v $(pwd)/qdrant_storage:/qdrant/storage:z qdrant/qdrant

Command 3

Run the data ingestion script:

    python ingest.py

Command 4

Start the FAST API server using uvicorn:

    uvicorn app:app
