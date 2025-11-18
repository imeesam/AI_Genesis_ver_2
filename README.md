# 🤖 Agentic AI Study & Research Copilot

![Banner Image](path/to/your/banner_image.png)

Intelligent AI assistant designed for **study and research**, capable of ingesting multi-modal content and providing context-aware answers through a Retrieval-Augmented Generation (RAG) pipeline.

---

## **1. User Input / Content Submission**

Users provide content in **three main formats**:

1. **PDF files** – upload academic papers, books, or reports.  
2. **Web URLs** – provide webpages containing articles, tutorials, or documentation.  
3. **YouTube links** – supply videos to transcribe and ingest content.  

Optional: direct text input for quick ingestion.  

**Purpose:** Capture all sources of study or research material to build a knowledge base.

---

## **2. Ingestion & Preprocessing**

* **PDF Ingestor:** Extracts text via PyMuPDF → chunks → embeddings.  
* **Web Ingestor:** Scrapes webpages → cleans → chunks → embeddings.  
* **YouTube Ingestor:** Downloads audio → transcribes via Whisper → cleans → chunks → embeddings.  

**Text Chunking:** Enables semantic search for large documents.  
**Embeddings:** Converts chunks into numerical vectors for retrieval.

**Purpose:** Standardize diverse data for semantic search by AI.

---

## **3. Vector Store / Knowledge Base**

* Stores all content embeddings.  
* Enables **semantic search**, retrieving relevant chunks even if query words don’t match exactly.  
* Supports updates, clearing, and re-ingestion of content.

**Purpose:** Efficient retrieval for answering queries accurately.

---

## **4. Query Handling & Agent Processing**

* **User Query:** Submitted via Streamlit frontend.  
* **RAG Pipeline:**
  1. **Retriever:** Finds relevant chunks from vector store.  
  2. **Agent / LLM:** Generates context-aware answers using retrieved content.

**Optional Features:**
* Parallel or sequential agents for multi-step reasoning.  
* Context compaction to handle large knowledge bases.

**Purpose:** Combine retrieval and generative AI for precise answers.

---

## **5. Response / Frontend Interaction**

* Answers displayed in **Streamlit chat interface**:
  * Live typing animation.  
  * Chat history maintained.  
* Users can clear sources or update ingestions anytime.  

**Purpose:** Natural and interactive AI-human experience leveraging stored knowledge.

---

## **6. Optional Management & Deployment**

* **Memory & Sessions:** Keeps long-term ingested content and session state.  
* **Deployment:**  
  * FastAPI backend + Streamlit frontend.  
  * Vector store can be cloud-hosted (Supabase / FAISS).  
  * Fully scalable and modular architecture.

**Purpose:** Ready for multi-user, scalable research deployment.

---

## **7. End-to-End Flow Overview**

![Mermaid Flow Diagram](path/to/your/mermaid_flow_image.png)

```mermaid
graph TD
A[User Uploads Content (PDF / Web / YouTube / Text)] --> B[Ingestor Module]
B --> C[Text Chunking & Embeddings]
C --> D[Vector Store / Knowledge Base]
E[User Query] --> F[RAG Pipeline]
D --> F
F --> G[LLM / Agent Generates Contextual Answer]
G --> H[Frontend Chat Interface (Streamlit)]
H --> I[User Sees Answer]
