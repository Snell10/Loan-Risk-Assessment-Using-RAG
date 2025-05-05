## 1.Introduction

This project presents a **Retrieval-Augmented Generation (RAG)** system for **loan risk evaluation**, converting structured credit data into case narratives and generating intelligent responses using open-source Large Language Models (LLMs). It simulates the judgment process of a human financial advisor, enabling explainable and context-aware loan eligibility recommendations.

---
## Dataset

https://www.kaggle.com/datasets/mpwolke/cusersmarildownloadsgermancsv
1.  Add this shortcut to drive
2.  This will allow us to link between Dataset and Drive.

---

## Project Structure
Loan_Risk_RAG/
*  german.csv # Source dataset (UCI German Credit Data)
*  Loan_Risk_Analysis_using_rag.ipynb # Main RAG pipeline notebook
*  chroma_loan_db/ # Persisted vector store
*  responses/ # Sample LLM outputs (optional folder)
*  results/ # Evaluation tables, charts, and logs
* README.md # Project documentation

- Step 1

1. **Clone this repository**
   
   git clone https://github.com/your-username/Loan_Risk_RAG.git
   
   cd Loan_Risk_RAG

-  Step 2
     
2. **Install Dependencies**

   pip install -U langchain langchain-community chromadb sentence-transformers transformers pandas

-  Step 3
  
3. **Run the Notebook**

   Loan_Risk_Analysis_using_rag.ipynb

## Language Models Used
| Model          | Type            | Source                                      | Use Case                      |
| -------------- | --------------- | ------------------------------------------- | ----------------------------- |
| FLAN-T5-Base   | Encoder-decoder | Hugging Face (`google/flan-t5-base`)        | Balanced general performance  |
| LaMini-Flan-T5 | Lightweight T5  | Hugging Face (`MBZUAI/LaMini-Flan-T5-248M`) | Fast & low-resource inference |
| Alpaca (7B)    | Decoder-only    | Replicate / HF (Stanford Alpaca)            | Most human-like & empathetic  |


## Example Questions
Sample domain-specific questions posed to the RAG system:
1. Is this applicant likely to repay the loan?
2. Does the applicant have any red flags?
3. What’s the impact of employment status on risk?
4. Should the loan be approved based on this profile?
5. Is this case similar to past approvals or defaults?

## Evaluation Metrics
* Factual Accuracy
* Reasoning Quality
* Empathy & Tone
* Response Relevance

Each model was scored from 1–5 based on its generated response across 10 loan-related scenarios.

## Environment

 * LangChain
 * ChromaDB
 * Transformers(Hugging Face)
 * Sentence Transformers
 * Python 3.10
 * Google Colab

## References
   
1.	Lewis et al., 2020. "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks."
2.	Raffel et al., 2020. "Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer."
3.	Touvron et al., 2023. "LLaMA: Open and Efficient Foundation Language Models."
4.	Chung et al., 2022. "Scaling Instruction-Finetuned Language Models."
5.	Borgeaud et al., 2022. "Improving Language Models by Retrieving from Trillions of Tokens."
6.	HuggingFace Transformers: https://huggingface.co/transformers/
7.	LangChain Documentation: https://docs.langchain.com/


