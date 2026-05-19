# 🎬 AskTube — YouTube Q&A Bot

Ask questions about any YouTube video using AI.

## How it works
1. Paste a YouTube URL → transcript is fetched automatically
2. Transcript is chunked and embedded into a vector store
3. Ask questions → relevant chunks are retrieved and answered by LLaMA 3 via Groq

## Tech Stack
- **Backend** — Flask, LangChain, FAISS
- **LLM** — LLaMA 3.3 70B via Groq (free)
- **Embeddings** — HuggingFace `all-MiniLM-L6-v2`
- **Frontend** — HTML, CSS, JavaScript

## Setup

1. Clone the repo
   ```bash
   git clone https://github.com/your-username/asktube.git
   cd asktube
   ```

2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```

3. Create `.env` from the example
   ```bash
   cp .env.example .env
   ```
   Then fill in your API keys:
   - **GROQ_API_KEY** → [console.groq.com](https://console.groq.com)
   - **HUGGINGFACE_API_KEY** → [huggingface.co/settings/tokens](https://huggingface.co/settings/tokens)

4. Run
   ```bash
   python app.py
   ```

5. Open [http://localhost:5000](http://localhost:5000)
