# RAG-Knowledge-Agent-ChatBot
This RAG workflow demonstrates a Knowledge agent chatbot built to address queries specific to a sample case study ( Nova cart company). It showcases how to make internal data(knowledge Source) searchable, controllable, & retrievable in a RAG framework ensuring the results are more trustworthy.

**Problem Statement**
The Scenario: NovaCart Global Commerce: NovaCart is a fast-growing consumer electronics company selling hardware (phones, smart hubs) and digital subscriptions.

The Pain Point : The leadership team at NovaCart meets weekly to discuss operational health. Currently, answering simple questions like:
-	 "Why did churn increase last week?" or
-	 "How does the NovaPhone X1 battery life compare to the new model?"
Current painful process:
1.  Data Silos: Financial metrics are locked in separate Word Document.
3.	Scattered Knowledge: Strategic context and product specs are buried in PDF Annual Reports and Word documents.
4.	Slow Turnaround: Analysts have to manually open these files, search for data, and write emails.
5.	Hallucinations: When staff try to use generic ChatGPT, it invents fake numbers because it doesn't have access to NovaCart's private internal data.

**Objective:**
Build a Retrieval-Augmented Generation (RAG) workflow that:
1.	Ingests metrics and documentation from multiple sources
2.	Embeds and indexes content for semantic retrieval
3.	Responds to user queries with grounded, source-cited answers only

**Goal**
Build an AI agent workflow using RAG framework. That will retrieve the necessary data from the internal knowledge sources attached and return a relevant message if the required data is not available in the source.

**Approach(high-level)**

1. We will use the **n8n platform** for building this workflow.
2. There will be one **Ingestion Pipeline** : for chunking and storing the Nova Cart's ( internal data ) in a Vector Database ( on Pinecone platform ).
   <img width="1107" height="532" alt="image" src="https://github.com/user-attachments/assets/23eb5f7c-f877-4b7c-8ade-d6324af8d0d5" />

3. We will have a **Retrieval Pipeline** : Upon a Chat trigger from the user agent(with system prompt) will use the LLM Model + Memory + Vector Db to search and retrieve the relevant data and publish the response to the user via same Chat Interface.
   <img width="1117" height="542" alt="image" src="https://github.com/user-attachments/assets/5468a5cf-3f0d-41c7-bb0e-b2783aed57dd" />


**System Design**
assets/RAG_simple.png

**Setup Instructions**
docs/Setup Instructions.md

**Scaling_Strategy**
docs/Scaling_Strategy.md

**Demo Video**




