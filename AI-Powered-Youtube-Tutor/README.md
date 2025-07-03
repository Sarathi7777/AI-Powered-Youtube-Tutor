# AI-Powered Tutor: YouTube Chatbot

This project is a Streamlit web app that allows you to ask questions about YouTube lecture transcripts using advanced language models. It retrieves the transcript from a YouTube video, processes it, and enables conversational Q&A.

## Features
- Extracts transcripts from YouTube videos
- Splits and embeds transcript text for retrieval
- Uses Anthropic Claude (via LangChain) as the LLM (default)
- Uses HuggingFace sentence-transformers for embeddings
- Interactive Q&A interface with Streamlit

## Setup Instructions

### 1. Clone the Repository
```bash
 git clone https://github.com/yourusername/GEN-AI-APP---Youtube-Chatbot-main.git
 cd GEN-AI-APP---Youtube-Chatbot-main
```

### 2. Create and Activate a Virtual Environment (Recommended)
```bash
python -m venv venv
# On Windows:
.\venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
pip install anthropic langchain-anthropic sentence-transformers
```

### 4. Set Up Environment Variables
Create a `.env` file in the project root with your Anthropic API key:
```
ANTHROPIC_API_KEY=your_anthropic_api_key_here
```

> **Note:** If you want to use OpenAI instead, update the code and set `OPENAI_API_KEY` in your `.env`.

### 5. Run the App
```bash
streamlit run app.py
```

The app will be available at [http://localhost:8501](http://localhost:8501).

## Usage
1. Enter a YouTube video URL (with available English transcript).
2. Click **Process Video** to extract and process the transcript.
3. Once processed, ask questions about the video content in the provided input box.

## Troubleshooting
- **Transcript Error:** Ensure the video has English transcripts enabled and is publicly available.
- **API Errors:** Make sure your API key is valid and you have sufficient quota.
- **Module Not Found:** Install missing dependencies with `pip install <package>`.

## Customization
- To use a different LLM or embedding provider, update the relevant imports and initialization in `app.py`.
- You can adjust chunk size and overlap in the `CharacterTextSplitter` for different transcript processing behavior.

## License
MIT License

## Credits
- [Streamlit](https://streamlit.io/)
- [LangChain](https://github.com/langchain-ai/langchain)
- [Anthropic Claude](https://www.anthropic.com/)
- [HuggingFace Sentence Transformers](https://www.sbert.net/)
- [pytube](https://github.com/pytube/pytube)
- [youtube-transcript-api](https://github.com/jdepoix/youtube-transcript-api)
