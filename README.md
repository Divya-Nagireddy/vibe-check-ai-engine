# Vibe Check: AI Semantic Search Engine

## The Concept
Traditional search engines rely on exact keyword matching (`Ctrl+F`). If a user searches for "a movie about a cold space station," traditional databases fail if the exact word "cold" isn't in the plot. 

I built a **Generative AI Recommender System** that understands the *meaning* of a user's search using **Vector Embeddings** and **Semantic Search**.

## 🛠️ The Tech Stack (RAG Architecture)
* **LLM Engine:** Google Gemini 2.5 Flash
* **Vector Database:** ChromaDB
* **Embeddings:** Hugging Face `all-MiniLM-L6-v2` (Sentence Transformers)
* **Data Source:** Hugging Face Datasets (Rotten Tomatoes)

## How it Works (Retrieval-Augmented Generation)
1. **Embedding:** The app translates 500 movie plots into 384-dimensional mathematical coordinates.
2. **Retrieval:** When a user types a "vibe" (e.g., "A wild teenage road trip"), the app translates the query and uses Cosine Similarity to find the 3 closest mathematical plots in ChromaDB.
3. **Augmented Generation:** The raw database results are injected into a dynamic prompt and sent to Gemini, which synthesizes a conversational, human-like recommendation for the user.
