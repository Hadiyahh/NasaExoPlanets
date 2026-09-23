# 🚀 A World Away

### NASA Exoplanet KOI Classification Platform

🥉 **3rd Place — NASA Space Apps Challenge (Local)**  
🌍 **Global Nominee**

A World Away is a full-stack machine-learning application that classifies **Kepler Objects of Interest (KOIs)** using data from NASA's Kepler mission.

The platform combines trained machine-learning models with a **FastAPI backend** and **React frontend** to provide an interactive way to explore exoplanet data and generate classification predictions.

▶️ **[Live App](https://nasa-exo-planets.vercel.app/)**  


<img width="920" height="443" alt="image" src="https://github.com/user-attachments/assets/11746277-d15c-4304-8b28-8df0dec7376c" />

---

## 🌌 Overview

NASA's Kepler mission identified thousands of **Kepler Objects of Interest (KOIs)** — signals that may represent potential planets orbiting distant stars.

A World Away explores how machine learning can help classify these objects as:

- **Candidate**
- **Confirmed Exoplanet**
- **False Positive**

The project combines:

- NASA Kepler DR25 data
- machine-learning classification
- a FastAPI prediction API
- an interactive React frontend
- researcher-oriented prediction tools
- educational content explaining exoplanets and the classification process

---

## 🧠 Machine Learning

The project explores two classification problems.

### Binary Classification

```text
Candidate
    vs.
False Positive
```

Models evaluated include:

- Logistic Regression
- Random Forest

### Multiclass Classification

```text
False Positive
      vs.
Candidate
      vs.
Confirmed Exoplanet
```

The models were trained using features from NASA's **Kepler DR25 cumulative KOI catalog**.

### High-Level Results

| Task | Model | Result |
|---|---|---|
| Binary Classification | Random Forest | F1 ≈ 0.92 |
| Multiclass Classification | Logistic Regression | Accuracy ≈ 0.91 |
| Multiclass Classification | Logistic Regression | Macro-F1 ≈ 0.87 |

The largest multiclass confusion occurred between **Candidate** and **Confirmed** objects.



---

## 🔄 How It Works

```text
NASA Kepler DR25 Dataset
          ↓
Data Cleaning & Preprocessing
          ↓
Feature Selection
          ↓
┌───────────────────────────┐
│ Logistic Regression       │
│ Random Forest             │
└───────────────────────────┘
          ↓
Trained Classification Model
          ↓
FastAPI Prediction API
          ↓
React Web Application
          ↓
KOI Classification
```

---

## 🔭 Researcher Interface

The researcher-facing interface allows users to enter astronomical parameters associated with a KOI.

Inputs include characteristics such as:

- orbital period
- transit duration
- transit depth
- planet-to-star radius ratio
- impact parameter
- estimated planetary radius
- signal-to-noise information
- false-positive indicators

These values are passed to the prediction backend and transformed into the feature structure expected by the trained model.

---

## ✨ Platform Features

### 🔬 KOI Classification

Users can enter relevant KOI parameters and submit them to the prediction API to receive a classification result.

### 🧑‍🔬 Researcher-Oriented Input

The application organizes model inputs into understandable groups such as:

- transit observables
- geometry and size
- signal quality
- system characteristics
- false-positive flags

### 🌌 Exoplanet Education

The site includes educational pages explaining:

- what exoplanets are
- how astronomers detect them
- the transit method
- Kepler Objects of Interest
- project architecture
- machine-learning classification

### 📄 Research Documentation

Detailed methodology and model results are separated into dedicated documentation so the main README remains easy to navigate.

---

## 🏗️ Architecture

```text
┌──────────────────────────────┐
│        React Frontend        │
│                              │
│ Home                         │
│ About Exoplanets             │
│ Researcher / Explorer        │
│ Project Structure            │
│ Extra Resources              │
└──────────────┬───────────────┘
               │
               │ HTTP / JSON
               ▼
┌──────────────────────────────┐
│         FastAPI API          │
│                              │
│ Input Validation             │
│ Prediction Endpoint          │
│ Model Integration            │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│    scikit-learn Models       │
│                              │
│ Logistic Regression          │
│ Random Forest                │
└──────────────┬───────────────┘
               │
               ▼
         Classification
```

---

## 🛠️ Tech Stack

| Area | Technology |
|---|---|
| **Frontend** | React, TypeScript, CSS |
| **Backend** | Python, FastAPI |
| **Machine Learning** | scikit-learn |
| **Models** | Logistic Regression, Random Forest |
| **Dataset** | NASA Kepler DR25 |
| **Deployment** | Vercel |
| **API Interface** | FastAPI / Swagger |
| **Version Control** | Git, GitHub |

---

## 👩‍💻 My Contribution

A World Away was developed collaboratively for the **NASA Space Apps Challenge**.

My work focused primarily on **frontend development, scientific research, early prediction-interface development, and application integration**.

I contributed to:

- Researched exoplanet transit detection, **Kepler Objects of Interest (KOIs)**, and the astronomical parameters used by the classifier
- Investigated how model inputs such as transit period, duration, depth, radius, signal quality, and false-positive indicators should be presented to users
- Built and refined major React pages, including:
  - Home
  - About Exoplanets
  - Project Structure
  - Extra Resources / Team
- Developed the application's navigation and frontend structure
- Worked on early versions of the **Researcher** and **Explorer** interfaces
- Contributed to frontend styling and layout
- Supported frontend/backend integration and debugging
- Modified FastAPI configuration during integration
- Resolved CORS issues affecting prediction requests
- Helped translate technical and astronomical concepts into understandable educational content

---

## 👥 Team

### 👩‍🚀 Mahnoz Akhtari — Machine Learning Engineer

Led machine-learning development, including model training, evaluation, and analysis of astronomical features for exoplanet classification.

### 👩‍💻 Hadiyah Arif — Software Engineer

Contributed to scientific research, React frontend development, early prediction-interface design, educational content, and frontend/backend integration.

### 🧑‍💻 Bobola Obiwale — Full-Stack Developer

Contributed to the FastAPI backend, model integration, prediction pipeline, frontend functionality, and deployment.

---

## 🧪 Model Evaluation

### Binary Classification

The binary task focuses on distinguishing:

```text
Candidate ↔ False Positive
```

The Random Forest model achieved approximately:

```text
F1 ≈ 0.92
```

without relying on leakage-prone features.

### Multiclass Classification

The multiclass task distinguishes:

```text
False Positive
Candidate
Confirmed
```

Logistic Regression achieved approximately:

```text
Accuracy ≈ 0.91
Macro-F1 ≈ 0.87
```

One of the main challenges was distinguishing **Candidate** objects from already **Confirmed** exoplanets using the available input features.


---

## 🏆 NASA Space Apps Challenge

A World Away was developed for the **NASA Space Apps Challenge** using NASA Kepler data.

The project received:

### 🥉 3rd Place — Local Challenge

and advanced as a:

### 🌍 Global Nominee

The challenge encouraged teams to use NASA data to develop solutions around real scientific and societal problems.

---

## 🚀 Running Locally

### Prerequisites

- Python 3
- Node.js
- npm
- pip

---

### Clone the Repository

```bash
git clone https://github.com/Hadiyahh/NasaExoPlanets.git
cd NasaExoPlanets
```

---

### Backend Setup

Create a virtual environment:

```bash
python3 -m venv .venv
```

Activate it.

#### Linux / macOS

```bash
source .venv/bin/activate
```

#### Windows

```bash
.venv\Scripts\activate
```

Install Python dependencies:

```bash
pip install -r requirements.txt
```

Start FastAPI:

```bash
uvicorn backend.app:app --reload
```

API documentation will be available at:

```text
http://localhost:8000/docs
```

---

### Frontend Setup

Navigate to the frontend:

```bash
cd frontend
npm install
npm run dev
```

---

## 📁 Project Structure

```text
NasaExoPlanets/
├── backend/
│   ├── app.py
│   ├── utils.py
│   ├── requirements.txt
│   ├── howToRun.md
│   └── dev.sh
│
├── data/
│   └── raw/
│
├── frontend/
│   ├── src/
│   ├── package.json
│   ├── vite.config.ts
│   └── ...
│
├── notebooks/
│   ├── models/
│   ├── baseline_model.ipynb
│   ├── modified_model.ipynb
│   ├── multiclass_analysis.ipynb
│   ├── multiclass_model.ipynb
│   └── preprocessing.ipynb
│
├── results/
├── README.md
├── requirements.txt
└── backend.dockerfile
```

---

## 📈 Project Status

### Completed

- ✅ NASA Kepler dataset processing
- ✅ Binary classification
- ✅ Multiclass classification
- ✅ Logistic Regression models
- ✅ Random Forest models
- ✅ FastAPI prediction backend
- ✅ React frontend
- ✅ Researcher-facing interface
- ✅ Educational exoplanet pages
- ✅ Live web deployment

### Future Improvements

- ⏳ SHAP-based model explanations
- ⏳ Per-KOI light-curve visualizations
- ⏳ More detailed model-confidence explanations
- ⏳ Expanded model comparison
- ⏳ Improved astronomical visualizations
- ⏳ Additional API validation
- ⏳ Improved mobile responsiveness

---

## 📚 Resources

- ▶️ [Live Application](https://nasa-exo-planets.vercel.app/)
- 🔭 [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/)

---

## 📄 License

This project is licensed under the **MIT License**.

---

## ⚠️ Disclaimer

A World Away is an educational hackathon project created to explore the application of machine learning to astronomical classification.

Predictions generated by the application are intended for demonstration and educational purposes and should **not** be treated as official confirmation or rejection of an exoplanet candidate.
