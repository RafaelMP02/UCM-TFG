# Conversacion con Don Francisco de Arobe

## English

### Project Name
Conversacion con Don Francisco de Arobe

### Description
This project is a Streamlit application that lets users chat with an AI persona of Don Francisco de Arobe, a historical figure from the 16th century.  
It uses Retrieval-Augmented Generation (RAG) over a PDF knowledge base to answer questions in Spanish with concise, in-character responses.  
The app also supports voice input (speech-to-text) and optional voice output (text-to-speech) with local models.

### Key Features
- Conversational RAG over PDF documents with persistent vector storage (Chroma or FAISS).
- Query contextualization with chat history and reranking using BGE/TART for better retrieval quality.
- Local LLM inference through `llama-cpp` (default) with configurable generation settings.
- Voice interaction pipeline: microphone transcription (Whisper) and synthesized responses (XTTS-v2).

### Tech Stack
- Python 3.11
- Streamlit
- LangChain ecosystem (`langchain`, `langchain-community`, `langchain-chroma`, `langchain-huggingface`)
- ChromaDB / FAISS
- `llama-cpp-python`, `transformers`, `sentence-transformers`
- `faster-whisper`, `TTS` (XTTS-v2), `sounddevice`, `pygame`
- Conda environment (`environment.yaml`)

### Quick Start
1. Create and activate the environment:
```bash
conda env create -f environment.yaml
conda activate tfg
```
2. Optional automated setup (installs extra runtime dependencies such as `llama-cpp-python` with CUDA):
```bash
bash install.sh
```
3. Ensure required local models exist under `./models` as configured in `config.yaml`.
4. Run the app:
```bash
streamlit run app.py
```

---

## Espanol

### Project Name
Conversacion con Don Francisco de Arobe

### Description
Este proyecto es una aplicacion Streamlit que permite conversar con una IA que representa a Don Francisco de Arobe, personaje historico del siglo XVI.  
Utiliza Retrieval-Augmented Generation (RAG) sobre una base documental en PDF para responder en espanol de forma breve y en primera persona.  
La aplicacion tambien admite entrada por voz (speech-to-text) y salida por voz opcional (text-to-speech) con modelos locales.

### Key Features
- RAG conversacional sobre documentos PDF con almacenamiento vectorial persistente (Chroma o FAISS).
- Contextualizacion de preguntas con historial de chat y reranking con BGE/TART para mejorar recuperacion.
- Inferencia local de LLM mediante `llama-cpp` (por defecto) con parametros configurables.
- Flujo de voz completo: transcripcion por microfono (Whisper) y sintesis de respuesta (XTTS-v2).

### Tech Stack
- Python 3.11
- Streamlit
- Ecosistema LangChain (`langchain`, `langchain-community`, `langchain-chroma`, `langchain-huggingface`)
- ChromaDB / FAISS
- `llama-cpp-python`, `transformers`, `sentence-transformers`
- `faster-whisper`, `TTS` (XTTS-v2), `sounddevice`, `pygame`
- Entorno Conda (`environment.yaml`)

### Quick Start
1. Crear y activar el entorno:
```bash
conda env create -f environment.yaml
conda activate tfg
```
2. Configuracion automatizada opcional (instala dependencias adicionales como `llama-cpp-python` con CUDA):
```bash
bash install.sh
```
3. Verificar que los modelos locales requeridos existan en `./models`, segun `config.yaml`.
4. Ejecutar la aplicacion:
```bash
streamlit run app.py
```
