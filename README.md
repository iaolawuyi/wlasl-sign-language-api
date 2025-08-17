# Sign Language to Text API

FastAPI-based REST API for real-time sign language to text conversion using a deep learning model.  
This project is part of my final year research work, **"Bridging Communication Gaps: A Sign Language to Text Conversion Model"**, aimed at helping bridge communication between the deaf community and non-signers.

---

## Features

- **Real-time Inference**: Send an image or video of a sign and receive the translated text.
- **Deep Learning Powered**: Uses a trained PyTorch model for accurate sign recognition.
- **Fast and Lightweight**: Built with FastAPI for high performance.
- **JSON Responses**: Easy integration with mobile, web, or other applications.

---

## Tech Stack

- **Backend Framework**: [FastAPI](https://fastapi.tiangolo.com/)
- **Model Serving**: PyTorch
- **Image Processing**: Pillow, OpenCV
- **Deployment**: Uvicorn, Docker (optional)

---

## Project Structure

asl-sign-language-api/
│── app/
│ ├── main.py # FastAPI entry point
│ ├── model.py # Model loading & inference
│ ├── preprocessing.py # Preprocessing utilities
│ ├── routes.py # API routes
│── requirements.txt
│── README.md


---

## Installation

1. **Clone the repository**
```bash
git clone https://github.com/iaolawuyi/wlasl-sign-language-api.git
cd wlasl-sign-language-api

2. **Create a virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

3. **Install dependencies**
```bash
pip install -r requirements.txt
