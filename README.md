# AGRISENSE-SMART-AGRICULTURE-WITH-WSN-AND-ML
# 🌱 Agrisense: Smart Agriculture with WSN & Machine Learning

## 📌 Project Overview

Agrisense is an IoT-based smart agriculture system that leverages **Wireless Sensor Networks (WSN)** and **Machine Learning (ML)** to optimize irrigation and improve crop yield.
Using **Arduino UNO**, **DHT11 temperature & humidity sensors**, and **soil moisture sensors**, the system collects real-time environmental data. This data is then analyzed using ML algorithms to provide actionable recommendations for farmers.

---

## ⚙️ Features

* Real-time monitoring of **temperature, humidity, and soil moisture**.
* Wireless data transmission from **Arduino-based sensor nodes**.
* **IoT integration** for data storage and visualization.
* **Machine Learning models (SVM, Random Forest, KNN, Decision Trees, K-Means)** for:

  * Irrigation optimization
  * Crop recommendation
  * Yield prediction

---

## 🛠️ Tech Stack

* **Hardware:** Arduino Uno, DHT11, Soil Moisture Sensor
* **Software:** Python, Pandas, NumPy, scikit-learn
* **ML Algorithms:** SVM, Random Forest, KNN, Decision Tree, K-Means Clustering
* **Visualization:** Matplotlib, Seaborn

---

## 📊 Workflow

1. **Data Collection:** Sensors collect temperature, humidity, and soil moisture values.
2. **Data Transmission:** Values are transmitted wirelessly via WSN modules (ESP8266 / LoRa / XBee).
3. **Data Storage:** Data is stored on a server or cloud (ThingsBoard / Flask API).
4. **Preprocessing:** Data cleaned and prepared using Pandas.
5. **Machine Learning Models:**

   * **KNN / Random Forest / SVM** → for irrigation decisions
   * **Decision Tree** → rule-based recommendation
   * **K-Means** → clustering soil conditions
6. **Recommendation System:** Suggests when & how much to irrigate for improved crop yield.

---


## 🚀 How to Run

### Arduino

1. Upload code from `Arduino_Code/agrisense.ino` to Arduino Uno.
2. Connect DHT11 & Soil Moisture sensor as per pin configuration.

### Machine Learning

```bash
# Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn flask
```

* Run any ML notebook in `ML_Models/` to train models.
* Example (Random Forest):

```python
from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier()
model.fit(X_train, y_train)
print("Accuracy:", model.score(X_test, y_test))
```

### Flask Backend

```bash
cd Backend
python app.py
```

* Access the API at `http://localhost:5000/predict`

---

## 📈 Results

* **Accuracy**: ~85–90% (Random Forest best performing)
* **Irrigation scheduling** optimized using ML.
* **Crop yield prediction** improved with environmental data.

---

## 📌 Future Enhancements

* Add **Fertilizer recommendation system**.
* Deploy ML models on **TinyML (Arduino Nano 33 BLE)** for edge inference.
* Build a **web/mobile dashboard** for farmers.


---

