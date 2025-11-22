# Text-Emotion-Classifier

A full-stack NLP application that classifies the emotional tone of user-generated text using Transformer-based models. Built with FastAPI, Streamlit, HuggingFace Transformers, SQLite, and SQLAlchemy, this project demonstrates real-time inference, visualizations, and database-backed prediction history.

🚀 Features

Dual-Model Emotion Detection
Uses both:
• michellejieli/emotion_text_classifier
• roberta-base-emotions-detection
Returns probability distributions across 7 emotions:
anger, disgust, fear, joy, neutral, sadness, surprise

Full-Stack Architecture

Backend: FastAPI inference pipeline + database storage

Frontend: Streamlit UI with visual charts

DB Layer: SQLAlchemy ORM + SQLite

Interactive Visualizations

Comparative bar charts

Emoji-mapped emotions

Realtime probability scores

Prediction History
Stores past classifications using a clean SQL schema and CRUD APIs.

📂 Tech Stack

Backend: FastAPI, SQLAlchemy, SQLite
Frontend: Streamlit, Matplotlib
NLP Models: HuggingFace Transformers
Languages: Python
Other: Requests, Pydantic

📁 Project Structure
project/
│── backend/
│   ├── main.py
│   ├── crud.py
│   ├── database.py
│   ├── model.py
│   ├── schemas.py
│
│── ml_models/
│   ├── pretrained_model.py
│   ├── pretrained_model_roberta.py
│
│── frontend/
│   ├── frontend_streamlit.py
│
│── app_run.py
│── README.md

🧠 How It Works

User enters text in Streamlit UI

UI sends request → FastAPI endpoint /classify-emotion/

Text is passed into 2 Transformer models

Softmax applied to generate probability outputs

Results stored in database via SQLAlchemy

Streamlit displays:

Probability bars

Emoji-coded emotions

History of past predictions

▶️ Run the Project
1️⃣ Install dependencies
pip install -r requirements.txt

2️⃣ Start Backend (FastAPI)
uvicorn backend.main:app --reload

3️⃣ Start Frontend (Streamlit)
streamlit run frontend/frontend_streamlit.py

4️⃣ Open App in Browser
http://localhost:8501

📊 Example Output

Emotion probabilities across 7 classes

Comparative visualization between two models

Stored historical predictions with exact probability values

📌 Use Cases

Customer feedback sentiment analysis

Mental health text analytics

Social media monitoring

Content moderation & safety

Behavioral trend analysis
