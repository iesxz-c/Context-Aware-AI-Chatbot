# Context Aware AI Chatbot

A powerful, intelligent AI chatbot powered by **Retrieval-Augmented Generation (RAG)** technology. This application combines semantic search with cutting-edge language models to deliver accurate, contextually relevant responses by retrieving information from a vector database.

## Overview

This chatbot leverages RAG architecture to overcome traditional LLM limitations by grounding responses in actual documents and data. Rather than relying solely on training data, it retrieves relevant information from a vector database in real-time, ensuring answers are current, accurate, and sourced from your knowledge base.

### Key Capabilities

- **Context-Aware Responses**: Retrieves relevant documents before generating answers
- **Multi-Source Integration**: Supports document ingestion via web scraping
- **Flexible AI Models**: Works with Google Gemini and OpenAI APIs
- **Vector Search**: Uses Astra DB for fast semantic similarity matching
- **Modern UI**: Responsive, animated interface with real-time chat streaming

## 🛠️ How to Run

1. Clone the repo:
```bash
git clone https://github.com/iesxz-c/VROOM-RAG.git
cd VROOM-RAG
cd rag
````

2. Install dependencies:

```bash
npm install
```

3. Create a `.env` file:

```env
GEMINI_API_KEY=your_api_key
ASTRA_DB_API_ENDPOINT=your_endpoint
ASTRA_DB_APPLICATION_TOKEN=your_token
ASTRA_DB_NAMESPACE=your_namespace
ASTRA_DB_COLLECTION=your_collection
```

4. Seed the database:

```bash
npm run seed
```

(This runs the `scripts/load_DB.ts` script to populate Astra DB.)

5. Start the dev server:

```bash
npm run dev
```

Then open [http://localhost:3000](http://localhost:3000) in your browser.

---

## Tech Stack

**Frontend**
- Next.js 14 (React framework)
- React 18 (UI library)
- TypeScript (type safety)
- Framer Motion (animations)

**Backend**
- Next.js API Routes
- Node.js runtime
- ts-node (TypeScript execution)

**AI & ML**
- Google Gemini API (primary LLM)
- OpenAI API (alternative)
- Vercel AI SDK (unified interface)
- LangChain (orchestration)

**Database & Storage**
- Astra DB by DataStax (vector & NoSQL database)
- Document embeddings for semantic search

**Web Tools**
- Puppeteer (web scraping for document ingestion)

## Architecture

```
User Input
    ↓
Chat Interface (Next.js/React)
    ↓
Query Embedding → Vector Search (Astra DB)
    ↓
Retrieved Documents (Context)
    ↓
Prompt Engineering + Context
    ↓
LLM Generation (Google Gemini)
    ↓
Streamed Response to User
```

Powered by:

* React + Next.js
* Google Gemini (for generation)
* Astra DB (for retrieval)

MIT License.

