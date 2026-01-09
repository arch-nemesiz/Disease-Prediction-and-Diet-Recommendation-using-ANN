# AI Disease Prediction & Health Assistant

An AI-powered healthcare web application that predicts diseases based on user-entered symptoms and provides disease descriptions, precautionary measures, AI-generated healthy Indian recipes, and an interactive health chatbot.

This project is built using Flask, Machine Learning, and Google Gemini AI, and is suitable for academic, learning, and portfolio use.

---

## Features

* Disease prediction using a trained machine learning model
* Natural language symptom input (comma-separated)
* Disease descriptions from structured medical datasets
* Precautionary measures for predicted diseases
* AI-generated healthy Indian recipes based on condition
* Interactive AI chatbot for health-related queries
* Cleaned and readable AI-generated responses

---

## Tech Stack

* Backend: Flask (Python)
* Machine Learning: Scikit-learn
* NLP: TF-IDF Vectorizer
* AI Model: Google Gemini 1.5 Flash
* Data Storage: CSV datasets
* Frontend: HTML with Jinja templates

---

## Project Structure

```
├── app.py
├── model.pkl
├── vectorizer.pkl
├── symptom_Description.csv
├── symptom_precaution.csv
├── templates/
│   └── index.html
├── static/
│   └── css / js / assets
└── README.md
```

---

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/ai-disease-prediction.git
cd ai-disease-prediction
```

### 2. Create a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install flask joblib pandas numpy scikit-learn google-generativeai
```

---

## Gemini API Configuration

You must configure a Google Gemini API key before running the application.

In `app.py`, replace:

```python
genai.configure(api_key="YOUR_API_KEY")
```

Recommended (secure) method using environment variables:

```bash
export GEMINI_API_KEY="your_api_key_here"
```

Then update the code to read from the environment.

---

## Running the Application

```bash
python app.py
```

Open your browser and navigate to:

```
http://127.0.0.1:5000
```

---

## Application Workflow

1. User enters symptoms separated by commas
2. Input text is vectorized using TF-IDF
3. Machine learning model predicts disease probabilities
4. Predicted disease is decoded using LabelEncoder
5. Disease description and precautions are retrieved from datasets
6. Gemini AI generates a suitable healthy Indian recipe
7. Chatbot endpoint processes user queries using Gemini AI

---

## Text Cleaning Logic

* Removes markdown formatting such as bold markers
* Normalizes excessive newlines
* Improves readability of AI-generated responses

---

## Disclaimer

This project is intended for educational and demonstration purposes only.
It does not provide medical diagnosis or treatment and should not replace professional medical advice.

---

## Future Enhancements

* Secure API key handling using environment variables
* Display prediction confidence scores
* Support for multiple disease predictions
* Improved frontend UI and UX
* Mobile-responsive design
* Deployment using Docker or cloud platforms

---

## Author

Rahul R
