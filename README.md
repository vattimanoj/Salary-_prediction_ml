# Salary-_prediction_ml
# Salary Prediction System

A production-style Flask web application that serves a trained Simple Linear Regression model to predict salary based on input features, built and deployed following a standard end-to-end machine learning workflow.

---

## Overview

This project demonstrates the complete lifecycle of a machine learning model — from training to deployment — packaged as a lightweight web service. A Simple Linear Regression model is trained offline, serialized with `pickle`, and served through a Flask API with an HTML front end for user interaction.

---

## End-to-End Workflow

The project was built following this sequence, which reflects the standard order for taking a model from development to production:

| Stage | Tool / Technology | Purpose |
|---|---|---|
| 1. Data Handling | Pandas, NumPy | Load and prepare the dataset |
| 2. Exploratory Analysis | Matplotlib | Visualize relationships in the data |
| 3. Model Training | scikit-learn (`LinearRegression`) | Fit the regression model |
| 4. Model Serialization | Pickle | Save the trained model as `slr_model.pkl` |
| 5. Application Layer | Flask | Build the API and serve the front end |
| 6. Front End | HTML (Jinja2 templates) | Collect input and display predictions |
| 7. Dependency Management | `requirements.txt` | Pin exact library versions |
| 8. Process Configuration | `Procfile` + Gunicorn | Define the production web server command |
| 9. Version Control | Git & GitHub | Track and host the source code |
| 10. Deployment | Render / Heroku / Railway | Serve the app publicly |

---

## Tech Stack

- **Language:** Python
- **ML Library:** scikit-learn
- **Web Framework:** Flask
- **Server (Production):** Gunicorn
- **Data Handling:** NumPy, Pandas

---

## Project Structure

```
├── app.py               # Flask application and prediction route
├── slr_model.pkl         # Serialized trained regression model
├── requirements.txt      # Python dependencies
├── Procfile               # Production start command for deployment
└── templates/
    └── index.html          # Web form for input/output
```

---

## How It Works

1. The user submits an input value through the web form.
2. Flask receives the request at the `/predict` endpoint.
3. The input is converted into a NumPy array and passed to the loaded model.
4. The model returns a predicted value.
5. The result is rendered back to the user on the same page.

---

## Local Setup

```bash
# 1. Clone the repository
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the application
python app.py
```

The app will be available at `http://127.0.0.1:5000/`.

---

## Deployment

The application is deployment-ready via the included `Procfile`:

```
web: gunicorn app:app
```

This makes it compatible with any platform supporting Gunicorn-based Python deployments, such as **Render**, **Heroku**, or **Railway**.

---

## Author

**[Vatti Manoj]**

- LinkedIn: [https://www.linkedin.com/in/manoj-vatti-ba952332a/]
- Live Project: [https://salary-prediction-ml-oxg7.onrender.com]

---

If this project was useful to you, consider leaving a star on the repository.
