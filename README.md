# Medical Document & Blood Test Analysis from PDF Reports

## Overview
This project provides an intelligent system for analyzing medical documents in PDF format, including laboratory reports, blood test results, medical summaries, and administrative healthcare documents.

The solution is based on a Retrieval-Augmented Generation (RAG) architecture, ensuring that all generated answers are strictly grounded in the content of the uploaded documents, with no external medical assumptions.

---

## Key Features
- Medical document analysis from **PDF reports**
- Support for:
  - Blood test results
  - Laboratory reports
  - Medical summaries
  - Administrative healthcare documents
- Reliable extraction of medical values and explanations
- Context-aware medical reasoning
- Strict grounding in document content
- Explicit handling of missing information

---

## Input & Output Specification

### Inputs
- Medical document in PDF format

### Outputs
- Structured and contextual medical explanations
- Interpretation of laboratory values when available
- Explicit indication when information is missing:
  - *“Data not available in the document.”*

---

## System Architecture & Pipeline

### Step 1 – PDF Content Extraction
- Documents processed page by page
- Extraction includes:
  - Laboratory values
  - Reference ranges
  - Medical notes
  - Administrative information

### Step 2 – Text Chunking and Vector Indexation
- Extracted text split into overlapping semantic chunks
- Sentence embeddings generated
- Indexed in a **FAISS vector database**

### Step 3 – Retrieval-Augmented Generation (RAG)
- Only the most relevant chunks are retrieved
- Prevents hallucinations and ensures factual grounding

### Step 4 – Context-Aware Medical Reasoning using LLM
- LLM generates structured explanations adapted to:
  - Blood tests
  - Lab reports
  - Medical summaries
- Missing data explicitly acknowledged

---

## Safety & Reliability
- No external medical knowledge injected
- Answers strictly grounded in document content
- Designed for transparency and medical safety

---

## Use Cases
- Understanding blood test results
- Navigating complex medical reports
- Patient-friendly explanations of medical documents
- Clinical and academic document analysis

---

## Technologies Used
- PDF text extraction tools
- Sentence Transformers
- FAISS
- Large Language Models
- Retrieval-Augmented Generation (RAG)

---

## Disclaimer
This system is intended for **informational and decision-support purposes only**.
It does **not replace professional medical diagnosis or consultation**.

---

## License
This project is intended for academic and research use.
