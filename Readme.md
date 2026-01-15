# 🍽️ FoodieBot - Intelligent Food Recommendation & Search System

**AI-powered food discovery using Vector Search, Metadata Filtering, and RAG Chatbots**

This project is an end-to-end **food recommendation and search system** that combines **semantic vector search (ChromaDB)**, **structured metadata filtering**, and an **enhanced Retrieval-Augmented Generation (RAG) chatbot** powered by large language models.

It demonstrates modern **agentic AI workflows**, production-style modularity, and explainable AI retrieval pipelines.

---

## ✨ Features

* 🔍 **Semantic Food Search** using sentence embeddings
* 🧠 **Advanced Filtering**

  * Cuisine-based filtering
  * Calorie constraints
  * Combined filters
* 🤖 **RAG-based Food Chatbot**

  * Context-aware responses
  * Food comparisons
  * Graceful fallbacks
* 💬 **Interactive CLI Interfaces**

  * Beginner-friendly chatbot
  * Advanced menu-driven search
* 🧩 **Modular & Reusable Architecture**

---

## 🗂️ Project Structure

```bash
.
├── advanced_search.py        # Advanced CLI search with filters
├── interactive_search.py     # Interactive food chatbot
├── enhanced_rag_chatbot.py   # RAG-based food assistant
├── calorie_checker.py        # Calorie-aware food search
├── result_limiter.py         # Result limiting & evaluation
├── shared_functions.py       # Core vector DB & search logic
├── FoodDataSet.json          # Food dataset
└── README.md
```

---

## 🧠 System Architecture

```text
User Query
   ↓
Sentence Transformer Embedding
   ↓
ChromaDB Vector Search (HNSW, Cosine)
   ↓
Metadata Filtering (Cuisine / Calories)
   ↓
Retrieved Context
   ↓
LLM (RAG) → Final Answer
```

---

## 📦 Core Components

### `shared_functions.py`

Core utility module responsible for:

* Loading and normalizing food data
* Creating and managing ChromaDB collections
* Generating embeddings
* Similarity search & filtered retrieval

---

### `interactive_search.py`

Interactive command-line chatbot for food discovery.

**Features:**

* Natural language queries
* Search history
* Help & suggestions

```bash
python interactive_search.py
```

---

### `advanced_search.py`

Menu-driven advanced food search interface.

**Search modes:**

1. Basic similarity search
2. Cuisine-based filtering
3. Calorie-based filtering
4. Combined filters
5. Demo mode

```bash
python advanced_search.py
```

---

### `enhanced_rag_chatbot.py`

Retrieval-Augmented Generation (RAG) chatbot.

**Capabilities:**

* Contextual food recommendations
* Food comparisons
* IBM Watsonx LLM integration
* Safe fallback responses

```bash
python enhanced_rag_chatbot.py
```

---

### `calorie_checker.py`

Utility for calorie-constrained food queries.

---

### `result_limiter.py`

Validation utility to test and limit search result sizes.

---

## 📊 Dataset Format

The system expects a JSON dataset with fields like:

```json
{
  "food_id": "1",
  "food_name": "Paneer Butter Masala",
  "food_description": "Creamy tomato-based curry",
  "food_ingredients": ["Paneer", "Tomato", "Butter"],
  "cuisine_type": "Indian",
  "food_calories_per_serving": 420
}
```

Missing fields are handled gracefully.

---

## ⚙️ Installation

### 1️⃣ Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate
```

### 2️⃣ Install Dependencies

```bash
pip install chromadb sentence-transformers numpy ibm-watsonx-ai
```

> ⚠️ IBM Watsonx credentials are required for the RAG chatbot.

---

## 🧪 Example Queries

* `Spicy vegetarian Indian food`
* `Low calorie Italian dishes`
* `Compare pizza and pasta`
* `Food under 300 calories`

---

## 🎯 What This Project Demonstrates

* Vector databases (ChromaDB)
* Semantic embeddings
* Metadata-aware retrieval
* Retrieval-Augmented Generation (RAG)
* CLI-based AI products
* Modular, production-ready design


---

## 📜 License

MIT License

---

## 👤 Author

Built by Chirag N Vijay with ❤️ for **applied AI, agentic workflows, and intelligent retrieval systems**.

---

