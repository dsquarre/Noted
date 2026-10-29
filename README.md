# Multilingual Meeting Transcription  
This project transcribes multilingual meeting audio using a combination of FastAPI (backend) and React (frontend), and is optimized for Linux-based systems.

---

## Tech Stack

- **Frontend**: React (Node.js & npm) - just for my future reference
- **Backend**: FastAPI (Python), with CORS middleware (not needed since react app build is run using fastapi)
- **fastapi_app**: React app build served using FASTAPI(python)
---

## Setup (Linux-based)

### 1. **Install dependencies**

```bash
sudo apt-get update
sudo apt-get install python3-pip ffmpeg fonts-noto-core
```

### 2. **Set up Python environment**

```bash
pip install virtualenv
virtualenv venv
source venv/bin/activate
pip install -r fastapi_app/requirements.txt
```

### 4. **fastapi_app setup**

```bash
cd fastapi_app
python main.py
```

> ⚠️ **IMPORTANT**: In `main.py`, configure your Gemini API key:
```python
genai.configure(api_key="YOUR_API_KEY")
```



## 📊 Benchmarks (i7 CPU, no GPU)

| Task                              | Audio Length | Time Taken  |
|-----------------------------------|--------------|-------------|
| Single Language (Tiny Model)      | 21 min       | ~2.5 min    |
| Dual Language (Tiny Model)        | 44 min       | ~35 min     |

> *GPU support and CUDA will drastically improve performance. Consider using the `base` model on systems with GPU.*

