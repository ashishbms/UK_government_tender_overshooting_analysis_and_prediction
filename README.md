# 🧠 Tender Overshoot Prediction — MLOps Project

A machine learning and MLOps pipeline to predict whether UK government e-tenders will **overshoot their estimated cost** based on tender metadata and descriptions. The system includes:

- 🧼 Data preprocessing and feature engineering
- 🧪 Model training and evaluation (Logistic Regression)
- 📦 Model tracking with MLflow
- 🐍 Packaged with `joblib`, Docker, and GitHub Actions
- 🖥️ Interactive frontend with **Streamlit**
- ☁️ Deployable via **Render**

---

## 🚀 Project Structure

```
tender-overshoot-mlops/
│
├── app/
│   └── streamlit_app.py       # Streamlit UI
│
├── data/
│   └── processed/             # Cleaned dataset used for training/inference
│
├── models/
│   └── model.pkl              # Trained ML model
│
├── scripts/
│   ├── preprocess.py          # Data cleaning and transformation pipeline
│   └── train_model.py         # Model training and MLflow tracking
│
├── mlruns/                    # MLflow artifacts and experiment logs
│
├── requirements.txt           # Python dependencies
├── Dockerfile                 # Docker setup for containerizing the app
├── render.yaml                # Render deployment configuration (if used)
└── README.md                  # You're here!
```

---

## 🔍 Problem Statement

Government e-tenders often exceed their initial cost estimates. This project helps predict such cost overshoots based on textual descriptions, regions, and other metadata — enabling risk scoring and smarter decision-making.

---

## 🛠️ Tools & Technologies

- **Python**, **Pandas**, **Scikit-learn**, **Joblib**
- **MLflow** for experiment tracking
- **Streamlit** for web UI
- **Docker** for containerization
- **GitHub Actions** for CI/CD
- **Render** for deployment

---

## 📦 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/KarthikGanesh1357/UK_government_tenders_prediction.git
cd UK_government_tenders_prediction
```

### 2. Set Up Virtual Environment

```bash
python -m venv venv
.\venv\Scripts\activate       # On Windows
# or
source venv/bin/activate      # On Linux/macOS
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run Preprocessing and Training

```bash
python scripts/preprocess.py
python scripts/train_model.py
```

---

## 🌐 Run Streamlit App Locally

```bash
streamlit run app/streamlit_app.py
```

---

## 🐳 Docker (Optional)

### Build and run locally:

```bash
docker build -t tender-app .
docker run -p 8501:8501 tender-app
```

---

## 🚀 Deployment (Render)

1. Push this project to GitHub
2. Connect GitHub repo to [Render](https://render.com/)
3. Use the following start command:

```
streamlit run app/streamlit_app.py
```

---

## 📊 MLflow Tracking

Start MLflow UI (optional):

```bash
mlflow ui
```

Then open [http://localhost:5000](http://localhost:5000) to view experiment logs.

---

## 🙌 Contributors

* **Karthik Ganesh** — Project Author and MLOps Pipeline Developer

---

## 📜 License

This project is licensed under the MIT License.
