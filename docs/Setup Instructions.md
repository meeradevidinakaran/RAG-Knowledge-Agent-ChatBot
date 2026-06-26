**Initial Steps**
Create an n8n account using your email id.
    1. you can use the n8n cloud 
    2. n8n self hosting using docker.
Create a Pinecone account - for Vector db instance and indexes. Generate API Key and store it.
Create a Cohere account - for re ranking strategy ( optional ). Generate API Key and store it.

Once Initial Steps are done continue to n8n for bulding the workflows.
**Workflow 1 - Ingestion Pipeline**
Use a manual trigger and connect it with the data node ( we will be accessing a Gdrive folder for a simple flow );Set up the credentials using your gmail id/ service accounts - download the files onto n8n instance.
Use the Pinecone node on n8n to connect to your pinecone instance via API Key. Connect the open AI model for embedding and Data loader for chunking.

**Workflow 2 - Retrieval Pipeline**
Use a Chat trigger connected to the Agent with clear system prompt instructions.
LLM model connection - In this example we are using OpenAI model linked using a valid API key.
Use a simple memory to store pre defined User chat text per session
Connect the Agent tool to Pinecone Vector db created during the Ingestion pipeline pointing to same index and namespace.
