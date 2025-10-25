# 🍏 Apple SEC Filing Scanner (NLP Pipeline)

## 🎯 Project Overview: Accelerated Due Diligence

This project is a **High-Throughput, AI-powered financial document analyzer** designed to rapidly extract actionable investment insights from large regulatory filings (like 10-K and 10-Q reports).

It converts hours of manual review into automated data signals, empowering analysts and quantitative models with faster intelligence.

***

## 🚀 Technical Architecture & Performance

The solution is engineered for speed and efficiency using a **Natural Language Processing (NLP) Pipeline** built on Python and the Hugging Face `transformers` library.

### ⚡️ Critical Performance Metric
The project was optimized using **GPU acceleration**, reducing the analysis time for a full 10-K document from **over 60 minutes (on CPU)** to **under 2 minutes (on a T4 GPU)**. This **~30x speed increase** is essential for scalable, daily document processing.

### 🧠 Model Stack
- **Summarization:** Utilizes the lightweight **`sshleifer/distilbart-cnn-12-6`** model to efficiently condense document chunks.
- **Signal Extraction:** Uses the **`distilbert-base-cased-distilled-squad`** model for Question Answering (QA) to precisely identify high-value information.

***

## 💡 Key Investment Signals Extracted

The final stage of the pipeline focuses the QA model on extracting specific factors critical to investment decisions:

- Revenue Jumps
- Cash-Flow Risks
- Buy/Sell Signals (General Risk Factors)

***

## 🛠️ Setup and Execution

### Prerequisites
1.  **Dependencies:** Ensure a T4 GPU runtime is active in Colab or a local environment is configured for CUDA.
2.  **Document:** Place the target SEC filing (e.g., `apple10k.pdf`) in the working directory.

### Installation
```bash
!pip install PyPDF2 transformers accelerate torch --quiet
