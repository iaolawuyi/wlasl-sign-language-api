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

```
asl-sign-language-api/
│── app/
│   ├── main.py          # FastAPI entry point
│   ├── model.py         # Model loading & inference
│   ├── preprocessing.py # Preprocessing utilities
│   ├── routes.py        # API routes
│── requirements.txt
│── README.md
```

---

## Installation

1. **Clone the repository**
```bash
git clone https://github.com/<your-username>/asl-sign-language-api.git
cd asl-sign-language-api
```

2. **Create a virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

---

## Running the API Locally

1. **Start the FastAPI server**
```bash
uvicorn app.main:app --reload
```

2. **Access the interactive API docs**
- Swagger UI: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
- ReDoc: [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

---

## Example API Usage

**Request**
```bash
curl -X POST "http://127.0.0.1:8000/predict/" -F "file=@example_sign.jpg"
```

**Response**
```json
{
  "predicted_class": "Hello"
}
```

---

## Roadmap

- [ ] Implement `/predict` endpoint for image input
- [ ] Add video-to-text translation
- [ ] Deploy to cloud (e.g., Render, Railway, Hugging Face Spaces)
- [ ] Add authentication for API usage
- [ ] Write unit tests

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- [FastAPI](https://fastapi.tiangolo.com/)
- [PyTorch](https://pytorch.org/)
- [Pillow](https://python-pillow.org/)
