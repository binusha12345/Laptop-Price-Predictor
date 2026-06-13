<div align="center">

# Laptop Price Predictor

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Scikit Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

An attractive Flask machine learning web app that predicts laptop prices from specifications such as RAM, weight, brand, laptop type, OS, CPU, GPU, touchscreen, and IPS display.

</div>

---

## Features

- Modern glassmorphism user interface
- Machine learning based price prediction
- Dedicated `model/` folder for notebook-based training work and the trained predictor
- Simple Flask backend
- Trained model saved as a pickle file
- Responsive laptop specification form
- Estimated price output in LKR
- Ready for deployment with `Procfile`

---

## Tech Stack

| Area | Technology |
| --- | --- |
| Backend | Python, Flask |
| Machine Learning | Scikit-learn, NumPy |
| Frontend | HTML, CSS |
| Model Format | Pickle |
| Deployment | Gunicorn / Procfile |

---

## Project Structure

```text
website/
+-- app.py                         # Flask application
+-- Procfile                       # Deployment command for Gunicorn
+-- README.md                      # Project documentation
+-- model/                         # Uploaded ML files used by the app
|   +-- model building.ipynb        # Jupyter notebook for model training
|   +-- predictor.pickle            # Saved trained prediction model
+-- static/
|   +-- style.css                   # Application styles
+-- templates/
|   +-- index.html                  # Main web page
+-- env/                           # Local virtual environment, not required in repo
```

---

## Uploaded Files

The latest uploaded project files are:

| File / Folder | Purpose |
| --- | --- |
| `app.py` | Flask backend that receives form data and returns the predicted laptop price |
| `Procfile` | Deployment file for running the app with Gunicorn |
| `README.md` | Documentation for the project |
| `model/model building.ipynb` | Jupyter Notebook used for model building and experimentation |
| `model/predictor.pickle` | Trained machine learning model loaded by the Flask app |
| `static/style.css` | Styling for the web interface |
| `templates/index.html` | Main HTML template for the prediction form |

The `env/` and `model/env/` folders are local virtual environments. They are useful on your computer, but they should normally be excluded from GitHub with `.gitignore`.

---

## Model Folder Highlight

The `model/` folder is an important part of this project because it contains both the machine learning development file and the saved model used by the website.

| File / Folder | Purpose |
| --- | --- |
| `model/model building.ipynb` | Main Jupyter Notebook used for data analysis, preprocessing, model training, and experimentation |
| `model/predictor.pickle` | Saved trained ML model generated from the notebook and loaded by `app.py` |

The notebook is useful for understanding how the model was created, while the pickle files are used to store and reuse the trained predictor without retraining every time.

---

## How It Works

1. The user enters laptop details in the web form.
2. Flask receives the form data through a POST request.
3. The input values are converted into a model-ready feature list.
4. The trained model from `model/predictor.pickle` predicts the laptop price.
5. The app displays the estimated price in Sri Lankan Rupees.

---

## Input Fields

| Field | Example |
| --- | --- |
| RAM | `8`, `16`, `32` |
| Weight | `1.5`, `2.2` |
| Company | Dell, HP, Apple, Lenovo, Asus |
| Type Name | Notebook, Gaming, Ultrabook, Workstation |
| Operating System | Windows, Mac, Linux, Other |
| CPU | Intel Core i3, i5, i7, AMD |
| GPU | Intel, AMD, Nvidia |
| Touchscreen | Yes / No |
| IPS Display | Yes / No |

---

## Run Locally

### 1. Clone or open the project

```bash
cd "Laptop Price Predictor"
```

### 2. Move into the web app folder

```bash
cd website
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

### 4. Activate the virtual environment

Windows:

```bash
venv\Scripts\activate
```

macOS / Linux:

```bash
source venv/bin/activate
```

### 5. Install dependencies

```bash
pip install flask numpy scikit-learn gunicorn
```

### 6. Start the app

```bash
python app.py
```

Open this URL in your browser:

```text
http://127.0.0.1:5000
```

---

## Deployment

The `website/Procfile` contains:

```text
web: gunicorn app:app
```

This can be used by platforms that support Procfile-based Python deployments.

---

## Model

This project includes both the training notebook and saved model files.

Training and experimentation file:

```text
model/model building.ipynb
```

Saved model used by the Flask website:

```text
model/predictor.pickle
```

In `app.py`, the model path is:

```python
filename = 'model/predictor.pickle'
```

---

## UI Preview

The app includes a dark glass-style interface with:

- Blue gradient background
- Smooth focus glow on inputs
- Animated prediction button
- Clean result display panel

---

## Future Improvements

- Add `requirements.txt`
- Add form validation for numeric inputs
- Fix the button text from `Precict Price` to `Predict Price`
- Add model performance metrics to the README
- Add screenshots of the web interface
- Add currency formatting for the predicted price

---

<div align="center">

Made with Python, Flask, and machine learning.

</div>
