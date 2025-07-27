# Medi_MultiModal_RAG
A medical chatbot which not only utilises text from the datasource but also uses the tables and images to provide more contextually rich and accurate results.

**Multimodal_RAG**
It is a Retrieval-Augmented Generation (RAG) pipeline that combines textual and visual modalities extracted from PDF documents. It generates multimodal embeddings, indexes them in a vector database, and uses them for context-aware question answering.

<img width="1822" height="518" alt="Screenshot 2025-07-28 at 4 21 51 AM" src="https://github.com/user-attachments/assets/a4cc08eb-21f9-43aa-a8ad-cbd89cd976fa" />

---

## 🧠 Workflow Overview

MULTIMODEL_USED: "openai/clip-vit-base-patch32"

1. **PDF Data Loading**  
   A case report or academic paper is downloaded and loaded locally.

2. **Text, Tables and Image Extraction**  
   - Text is extracted from PDF using PyMuPDF.
   - Images (if any) are also extracted for embedding.
   - Table

3. **Embedding Generation**  

   - Generates embeddings for text using language models.
   - Optionally uses image encoders for visual content.

4. **Vector DB Creation**  
   - FAISS is used for indexing the embeddings.
   - Metadata is attached to each chunk for later retrieval.

5. **Querying via RAG**  
   - A user query is embedded.
   - Top-k relevant chunks are retrieved using vector similarity.
   - Retrieved context is used to generate a final response.

---

## 🛠️ Dependencies

Install required packages using:

```bash
pip install -r requirements_01.txt
```
