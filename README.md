# Airfoil Regression with Flask

This project is a **Flask-based web application** for predicting airfoil pressure using a trained regression model. The model is loaded from a `pickle` file and provides predictions based on user input.

## Features
- **Web Interface:** Users can input features via a web form.
- **API Endpoint:** Allows making predictions using a JSON request.
- **Machine Learning Model:** Uses a pre-trained regression model to predict airfoil pressure.
- **Minimalist Flask App:** Easy-to-use and extendable for further improvements.

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/airfoil-regression.git
   cd airfoil-regression
   ```

2. Create and activate a virtual environment (optional but recommended):
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```

## Project Structure
```
.
├── model.pkl              # Trained regression model
├── templates
│   ├── home.html         # HTML template for web UI
├── Procfile
├── app.py                # Main Flask application
├── requirements.txt      # List of dependencies
├── README.md             # Project documentation
```

## Usage

### Running the Web App
```sh
python app.py
```
Visit `http://127.0.0.1:5000/` in your browser.

### API Endpoint
Send a POST request to `http://127.0.0.1:5000/predict_api` with JSON data:
```json
{
  "data": {
    "feature1": value,
    "feature2": value,
    "feature3": value
  }
}
```
Response:
```json
{
  "prediction": value
}
```

## Requirements
Ensure you have Python installed, then install dependencies from `requirements.txt`:

```
Flask
Gunicorn
Jinja2
Werkzeug
numpy
pandas
scipy
scikit-learn
matplotlib
```

## Deployment
To deploy using **Gunicorn**:
```sh
pip install gunicorn

gunicorn -w 4 -b 0.0.0.0:5000 app:app
```

## License
This project is open-source and available under the **MIT License**.

---
Feel free to contribute by submitting a pull request!

