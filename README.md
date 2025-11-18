# 🤖 Agentic AI Study & Research Copilot

<img src="frontend/banner.PNG" alt="Banner Image" width="700"/>

Intelligent AI assistant for **study and research**, capable of ingesting multi-modal content and providing context-aware answers via a **Retrieval-Augmented Generation (RAG) pipeline**.

---

## 1️⃣ User Input / Content Submission

Users provide content in **three main formats**:

1. **PDF files** – upload academic papers, books, or reports.  
2. **Web URLs** – provide webpages containing articles, tutorials, or documentation.  
3. **YouTube links** – supply videos to transcribe and ingest content.  

Optional: direct text input for quick ingestion.  

**Purpose:** Capture all sources of study or research material to build a comprehensive knowledge base.

---

## 2️⃣ Ingestion & Preprocessing

* **PDF Ingestor:** Extracts text via PyMuPDF → chunks → embeddings.  
* **Web Ingestor:** Scrapes webpages → cleans → chunks → embeddings.  
* **YouTube Ingestor:** Downloads audio → transcribes via Whisper → cleans → chunks → embeddings.  

**Text Chunking:** Enables semantic search for large documents.  
**Embeddings:** Converts chunks into numerical vectors for retrieval.

**Purpose:** Standardize diverse data for effective semantic search by AI.

---

## 3️⃣ Vector Store / Knowledge Base

* Stores all content embeddings.  
* Enables **semantic search**, retrieving relevant chunks even if query words don’t match exactly.  
* Supports updates, clearing, and re-ingestion of content.

**Purpose:** Efficient retrieval for accurate and context-aware answers.

---

## 4️⃣ Query Handling & Agent Processing

* **User Query:** Submitted via Streamlit frontend.  
* **RAG Pipeline:**
  1. **Retriever:** Finds relevant chunks from vector store.  
  2. **Agent / LLM:** Generates context-aware answers using retrieved content.

**Optional Features:**
* Parallel or sequential agents for multi-step reasoning.  
* Context compaction to handle large knowledge bases.

**Purpose:** Combine retrieval and generative AI for precise answers.

---

## 5️⃣ Response / Frontend Interaction

* Answers displayed in **Streamlit chat interface**:
  * Live typing animation.  
  * Chat history maintained.  

<img src="frontend/Chatinterface.jpeg" alt="Chat Interface" width="500"/>

**Purpose:** Natural and interactive AI-human experience leveraging stored knowledge.

---

## 6️⃣ Optional Management & Deployment

* **Memory & Sessions:** Maintains long-term ingested content and session state.  
* **Deployment:**  
  * FastAPI backend + Streamlit frontend  
  * Vector store can be cloud-hosted (Supabase / FAISS)  
  * Fully scalable and modular architecture

**Purpose:** Ready for multi-user, scalable research deployment.

---

## 7️⃣ End-to-End Flow Overview

<img src="frontend/FLOW.png" alt="Mermaid Flow Diagram" width="600"/>

PPT link: [Click here](https://gamma.app/docs/Agentic-AI-Study-Research-Copilot-k2tsgwk9h27x8fq)

---

© All Rights Reserved 2025 @mees.ai
