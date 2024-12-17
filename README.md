# Crime Prediction API

A **Flask-based API** to predict crime scores based on geographic location using a machine learning model trained on a **UK police dataset**. The API takes latitude and longitude as input and predicts a crime score out of 10, helping users evaluate property safety when purchasing a house.

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-2.0.3-black?style=flat&logo=flask&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-1.4.3-blue?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-1.22.4-lightgrey?style=flat&logo=numpy&logoColor=white)

---

## Features
- **POST API endpoint** to predict crime scores based on latitude and longitude.
- Utilizes **Pandas** and **NumPy** for data handling.
- Deployed on **Render** for easy access.

---

## Tech Stack
- **Backend**: Flask
- **Data Processing**: Pandas, NumPy
- **Deployment**: Render

---

## API Endpoint
The API is live at: [https://crimeprediction-pk3f.onrender.com/predict](https://crimeprediction-pk3f.onrender.com/predict)

---

## Request & Response

### 1. Input
Send a **POST** request with JSON input containing the following fields:

```json
{
  "longitute": "0.15",
  "latitude": "54.5150"
}
```

### 2. Output
The API responds with the **predicted crime score** out of 10:

```json
{
  "crime_score": 3.37,
  "longitute": "0.15",
  "latitude": "54.5150"
}
```

---

## Example Usage

You can test the API using tools like **cURL**, **Postman**, or Python's `requests` library.

### cURL Example:
```bash
curl -X POST https://crimeprediction-pk3f.onrender.com/predict \
     -H "Content-Type: application/json" \
     -d '{"longitute": "0.15", "latitude": "54.5150"}'
```

### Python Example:
```python
import requests

url = "https://crimeprediction-pk3f.onrender.com/predict"
data = {
    "longitute": "0.15",
    "latitude": "54.5150"
}
response = requests.post(url, json=data)
print(response.json())
```

### Response:
```json
{
  "crime_score": 3.37,
  "longitute": "0.15",
  "latitude": "54.5150"
}
```

---

## Use Case
This API is designed to assist users in evaluating property safety for a **property-selling Android app**. The crime score helps users identify locations suitable for their needs.

---

## Dataset
The dataset was sourced from **UK Police**. [Link to Dataset](https://data.police.uk/)

---

## Deployment
Deployed using [Render](https://render.com/).

---

## Contributing
Feel free to fork the repository, create a new branch, and submit a pull request to enhance the project.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Acknowledgments
- UK Police for providing the dataset.
- Flask, Pandas, and NumPy for powering the project.

---

*Created with ❤️ by [Sakib Ahmed Shanto](https://github.com/sakibahmedshanto)*
