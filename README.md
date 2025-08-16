# 📊 Churn Prediction Assistant

An end-to-end **customer churn prediction assistant** combining:

- Logistic Regression trained churn model (`log_reg_with_encoders.pkl`)
- **FastAPI** backend for predictions
- **Groq LLM** integration to convert natural language queries into structured features
- **Streamlit UI** for an interactive dashboard and chatbot

---

## 🚀 Features

- Predict customer churn probability directly via JSON input
- Ask in natural language (chatbot powered by Groq LLM)
- Generate actionable insights to reduce churn risk
- Simple web app interface with Streamlit

---

## 🛠️ Tech Stack

- **FastAPI** for REST API
- **Streamlit** for web frontend
- **Scikit-learn** for Logistic Regression model
- **Groq LLM** for natural language → structured JSON
- **pandas, joblib** for preprocessing

---

## 📂 Repository Structure
├── api.py # FastAPI backend

├── chatbot_llm.py # Groq LLM wrapper for JSON extraction

├── streamlit_app.py # Streamlit frontend

├── log_reg_with_encoders.pkl # Trained churn prediction model

├── requirements.txt # Dependencies

└── AI-Powered Assistant for Churn # Project documentation

---

## ⚙️ Requirements

- Python 3.9+
- Virtual environment recommended

Dependencies are listed in `requirements.txt`:

---


---
## ▶️ Quickstart Guide

Follow these steps to get the application running locally.  
You can copy–paste the entire block below into your terminal.

```bash
# 1. Clone the repository
git clone https://github.com/Anan651/churn-prediction-assistant.git
cd churn-prediction-assistant

# 2. Create virtual environment
(If you are using anaconda : conda create --name env )
python -m venv venv

# 3. Activate virtual environment
(for anaconda : conda activate env)
# venv\Scripts\activate

# 4. Install dependencies
pip install -r requirements.txt

# 5. Create a .env file in project root with the following content:
# (edit GROQ_API_KEY with your key)
Inside the .env
API_URL=http://localhost:8080
GROQ_API_KEY=your_groq_api_key_here


# 6. Run the FastAPI backend
uvicorn api:app --reload --host 0.0.0.0 --port 8080

# 7. In a new terminal (keep FastAPI running), start the Streamlit app
# Make sure virtualenv is activated in this terminal as well
streamlit run streamlit_app.py

