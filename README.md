# ⚡ GenAI: Sustainability Operations for Business Efficiency

An AI-powered business advisory system that helps **identify, assess, and act on operational inefficiencies**—focusing on **inventory waste and mismanagement** and **energy inefficiency**. This tool estimates the *cost of inaction* and generates tailored, SDG-aligned solutions that promote both sustainability and profitability, estimating ROI by leveraging information about available rebates, cost-efficient solutions, and current taxes. 

> 🏁 Built as part of the **Kaggle x Google Cloud GenAI 5-Day Intensive Capstone Challenge**.

---

## ✨ Key Features

- 🧠 **Natural Language Understanding** – Accepts freeform business descriptions and structured inputs.
- 📊 **Cost of Inaction Estimator** – Predicts operational losses due to inefficiency or inaction.
- 📚 **RAG-Enhanced Reasoning** – Uses a vector database (ChromaDB) to retrieve relevant business cases and solutions.
- 🛠 **LangGraph Agent Workflow** – Modular, explainable pipeline with intelligent branching and memory.
- 🌍 **SDG Alignment** – Solutions are framed to support UN Sustainable Development Goals (SDG 7, 12, 13).
- 📄 **Structured Reports** – Outputs actionable, business-friendly advisory summaries in JSON or markdown.

---

## Architecture Overview
[🔀 LangGraph Agent]
   ├── Node 1: Classifier
   │     → Inventory Waste OR Energy Inefficiency?
   ├── Node 2: RAG Retriever for Inventory
   ├── Node 3: RAG Retriever for Energy
   ├── Node 4: Inaction Cost Estimator
   ├── Node 5: Solution Generator
   └── Node 6: Report Composer

Each node uses either Gemini-generated logic or external data retrieval (via ChromaDB) to perform a specific sub-task. The agent workflow returns a full advisory report based on the selected path.

---

## 🛠️ Tech Stack

| Component                | Description                                      |
|-------------------------|--------------------------------------------------|
| `LangGraph`             | Agent orchestration and branching logic         |
| `Gemini API (Google)`   | Content generation, embeddings, RAG, and NLU    |
| `ChromaDB`              | Vector database to store and retrieve documents |
| `PDFPlumber`            | PDF text extraction for cases                   |
| `LangChain`             | Tooling and prompt abstraction                  |
| `Google Colab / Kaggle` | Notebook-based development and execution        |

---

## 🚀 How It Works

1. **User Input**: The user provides a structured + freeform business profile.
2. **Classification**: The agent classifies the inefficiency type.
3. **Retrieval (RAG)**: It pulls relevant cases from the ChromaDB vector store.
4. **Estimation**: Gemini estimates losses ($) if no corrective action is taken.
5. **Solution Generation**: Generating multiple tailored, sustainable solutions.
6. **Report Composition**: A final, structured advisory report is generated.

---

📈 Potential Applications and Scalability
- Small businesses aiming to reduce waste and costs
- Sustainability consultants needing data-backed insights
- Government grant reporting aligned with SDGs
- Large retailers looking to optimize operations across locations

