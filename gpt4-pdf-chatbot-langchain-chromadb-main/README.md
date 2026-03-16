# GPT-4 PDF Chatbot using LangChain & Chroma

This project builds an AI chatbot that can answer questions from your documents such as PDF, DOCX, PPTX, HTML, TXT, and CSV files.

It uses OpenAI GPT-4 / GPT-3.5 with LangChain and Chroma Vector Database to convert documents into embeddings and retrieve relevant information during conversations.

Users can upload documents and interact with them through a ChatGPT-style interface.

---

# Tech Stack

- Next.js
- TypeScript
- LangChain
- OpenAI API
- ChromaDB (Vector Database)
- Tailwind CSS

---

# Features

- Chat with your documents
- Supports multiple file formats:
  - PDF
  - DOCX
  - PPTX
  - TXT
  - CSV
  - HTML
- Supports multiple documents
- Uses Chroma open-source vector database
- Uses GPT-4 or GPT-3.5
- Local document embedding (your data stays local)

---

# Prerequisites

Make sure you have:

- Node.js v18 or higher
- Docker installed
- OpenAI API key

Check Node version:

```
node -v
```

---

# Installation

## 1. Clone the Repository

```
git clone https://github.com/YOUR_USERNAME/gpt4-pdf-chatbot.git
cd gpt4-pdf-chatbot
```

---

## 2. Install Dependencies

Install yarn globally if not installed:

```
npm install -g yarn
```

Then install packages:

```
yarn install
```

After installation you should see:

```
node_modules
```

---

# Environment Setup

Create a `.env` file by copying:

```
.env.example
```

Example `.env` file:

```
OPENAI_API_KEY=your_openai_key
COLLECTION_NAME=your_uuid
```

Generate UUID using:

```
uuidgen
```

---

# Start Chroma Database

Run Chroma locally using Docker:

```
git clone https://github.com/chroma-core/chroma.git
cd chroma
docker-compose up -d --build
```

This starts the Chroma vector database server.

---

# Add Documents

Place your files inside the `docs` folder.

Supported formats:

- PDF
- DOCX
- PPTX
- TXT
- CSV
- HTML

---

# Convert Documents to Embeddings

Run the ingestion script:

```
npm run ingest
```

This converts your documents into embeddings and stores them in ChromaDB.

---

# Run the Application

Start the development server:

```
npm run dev
```

Open in browser:

```
http://localhost:3000
```

You can now chat with your documents.

---

# Customization

Modify the prompt used by the AI in:

```
utils/makechain.ts
```

To use GPT-4 change:

```
modelName: "gpt-4"
```

Make sure your OpenAI account has GPT-4 API access.

---

# Troubleshooting

If the project fails:

- Ensure Node version ≥ 18
- Verify `.env` variables are correct
- Confirm OpenAI API key is valid
- Ensure Docker is running
- Check Chroma server logs
- Make sure you have OpenAI credits

---
