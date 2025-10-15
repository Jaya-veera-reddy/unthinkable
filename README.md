# Audio Transcription and Summarization Web Application

## Overview
This project is a Flask-based web application that provides audio transcription and summarization functionalities. Users can upload audio files, which are transcribed into text and then summarized to provide actionable insights. The application integrates modular Python scripts for transcription and summarization, ensuring reusability and maintainability.

---

## Features
- **Audio Transcription:**
  - Handles large audio files by splitting them into smaller chunks.
  - Uses Google Speech Recognition for accurate transcription.

- **Text Summarization:**
  - Summarizes the transcribed text using the Ollama LLM.
  - Provides detailed summaries with task assignments and responsibilities.

- **Web Interface:**
  - User-friendly interface for uploading audio files.
  - Displays both the transcript and the summarized output.

---

## File Structure
```
project-root/
├── app.py                  # Flask web application
├── large_audio_transcribe.py # Script for audio transcription
├── ollama_summarize.py     # Script for text summarization
├── __pycache__/            # Compiled Python files
└── README.md               # Project documentation
```

---

## Installation

### Prerequisites
- Python 3.8 or higher
- Pip (Python package manager)

### Steps
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Flask application:
   ```bash
   python app.py
   ```

4. Open your browser and navigate to:
   ```
   http://127.0.0.1:5000
   ```

---

## Usage
1. Upload an audio file through the web interface.
2. Wait for the transcription and summarization process to complete.
3. View the transcript and summarized output on the results page.

---

## Scripts

### `large_audio_transcribe.py`
- **Purpose:** Transcribes large audio files by splitting them into smaller chunks.
- **Function:** `transcribe_audio(file_path)`
  - Input: Path to the audio file.
  - Output: Full transcript as a string.

### `ollama_summarize.py`
- **Purpose:** Summarizes the transcript using the Ollama LLM.
- **Function:** `summarize_transcript(transcript)`
  - Input: Transcript text.
  - Output: Summarized text as a string.

### `app.py`
- **Purpose:** Flask web application to integrate transcription and summarization.
- **Routes:**
  - `/`: Home page with upload form.
  - `/upload`: Handles file uploads and triggers transcription and summarization.

---

## Dependencies
- Flask
- Google Speech Recognition
- Pydub
- Ollama LLM API

---

## Future Enhancements
- Add support for multiple languages in transcription and summarization.
- Implement user authentication for personalized experiences.
- Provide downloadable results in text or PDF format.

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## Acknowledgments
- [Flask](https://flask.palletsprojects.com/)
- [Google Speech Recognition](https://pypi.org/project/SpeechRecognition/)
- [Pydub](https://pypi.org/project/pydub/)
- [Ollama LLM](https://ollama.ai/)
