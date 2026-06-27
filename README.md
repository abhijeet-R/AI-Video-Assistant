# 🎬 AI Video Assistant

AI Video Assistant is a meeting intelligence application that turns long audio or video recordings into useful, actionable information. Instead of manually listening through an entire meeting, you can upload a local recording or provide a YouTube link, and the application will generate a transcript, summarize the discussion, extract important action items and decisions, and even let you ask questions about the meeting using Retrieval-Augmented Generation (RAG).

This project was built using **Python, Streamlit, LangChain, Whisper, Mistral AI, and ChromaDB**.

---

## Features

* 🎥 Process YouTube videos or local audio/video files
* 📝 Generate accurate meeting transcripts with Whisper
* 🌐 Hinglish transcription support using Sarvam AI
* 📋 Create concise AI-generated meeting summaries
* 🏷️ Automatically generate meeting titles
* ✅ Extract action items
* 🔑 Identify key decisions
* ❓ Highlight unanswered questions and follow-ups
* 💬 Chat with the meeting transcript using RAG

---

## How it Works

The application follows a simple pipeline:

1. Extract audio from a YouTube link or local media file.
2. Convert the audio into a suitable format.
3. Split long recordings into manageable chunks.
4. Generate a transcript using Whisper (or Sarvam AI for Hinglish).
5. Produce a meeting title and summary using Mistral AI.
6. Extract action items, key decisions, and open questions.
7. Build a vector database using ChromaDB.
8. Allow users to ask natural language questions about the meeting.

---

## Tech Stack

### Frontend

* Streamlit

### AI & LLM

* OpenAI Whisper
* Mistral AI
* LangChain

### RAG

* ChromaDB
* HuggingFace Embeddings
* Sentence Transformers

### Audio Processing

* yt-dlp
* pydub
* FFmpeg

### Language

* Python

---

## Project Structure

```
AI-Video-Assistant/
│
├── app.py
├── main.py
├── requirements.txt
│
├── core/
│   ├── extractor.py
│   ├── rag_engine.py
│   ├── summarizer.py
│   ├── transcriber.py
│   └── vector_store.py
│
├── utils/
│   └── audio_processor.py
│
├── downloads/
├── vector_db/
└── README.md
```

---

## Getting Started

Clone the repository.

```bash
git clone https://github.com/abhijeet-R/AI-Video-Assistant.git
cd AI-Video-Assistant
```

Create a virtual environment.

```bash
uv venv
```

Activate it.

**Windows**

```bash
.venv\Scripts\activate
```

**Linux / macOS**

```bash
source .venv/bin/activate
```

Install the required packages.

```bash
uv pip install -r requirements.txt
```


## FFmpeg

This project uses FFmpeg for audio conversion.

Download FFmpeg from:

https://ffmpeg.org/download.html

Make sure FFmpeg is available in your system PATH.

Verify the installation:

```bash
ffmpeg -version
```

---

## Running the Application

To launch the Streamlit interface:

```bash
streamlit run app.py
```

---

## Example Inputs

**YouTube**

```
https://www.youtube.com/watch?v=...
```

**Local File**

```
meeting.mp4
meeting.wav
meeting.mp3
```

---

## Future Improvements

Some features I'd like to add in the future include:

* Speaker diarization
* Support for additional languages
* Export summaries as PDF
* Meeting history and search
* Cloud deployment
* Authentication
* Multi-meeting semantic search

---

## Requirements

* Python 3.10+
* FFmpeg
* Mistral API Key
* Sarvam AI API Key (optional for Hinglish)


---

If you found this project useful or have suggestions for improvement, feel free to open an issue or contribute.
