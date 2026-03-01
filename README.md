# Multi-Stage RAG Failover Agent

## Overview

This project implements a **Multi-Stage Retrieval-Augmented Generation  Failover Agent** for handling ambiguous or out-of-domain queries robustly.  
The system follows a structured retrieval pipeline:

**Strict → Broad → Query Expansion → Context-only Synthesis → Final Refusal**

The architecture ensures:
  High factual accuracy  
  Minimal hallucination  
  Safe handling of unknown queries  

---

## Features

  **R1 – High Threshold Retrieval:** Retrieves highly relevant documents using a strict TF-IDF threshold.  
  **R2 – Broad Fallback Retrieval:** Uses a lower threshold to improve recall when strict retrieval fails.  
  **R3 – Query Expansion:** Expands ambiguous or short queries to improve retrieval.  
  **R4 – Context-only Synthesis:** Generates answers strictly from retrieved documents.  
  **R5 – Final Refusal Logic:** Refuses to answer if no relevant context is found.

---

## Technology Stack

  **Python 3.x**  
  **scikit-learn** (TF-IDF Vectorizer & Cosine Similarity)  
  **NumPy**  
  **Google Colab** (optional)  

---

## How It Works

1. **Strict Retrieval:** Finds top matching documents with a high similarity threshold.  
2. **Broad Retrieval:** If strict fails, lowers threshold to include more documents.  
3. **Query Expansion:** Expands ambiguous queries using predefined rules.  
4. **Context-only Synthesis:** Concatenates retrieved documents into a structured answer.  
5. **Final Refusal:** If no documents are relevant, returns a safe refusal message.

---

## Example Queries & Output

User Query 

 What is RAG? 
 Explain failover system 
 How to prevent hallucination?
 Tell me about quantum physics 

---

## Author

## Mageshwari K
## Kanagalakshimi P
