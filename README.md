
# 🌱 Agrisense: Smart Agriculture with WSN & Machine Learning

## 📌 Project Overview

Agrisense is an IoT-based smart agriculture system that leverages **Wireless Sensor Networks (WSN)** and **Machine Learning (ML)** to optimize irrigation and improve crop yield.

Using **Arduino UNO**, **DHT11 temperature & humidity sensors**, and **soil moisture sensors**, the system collects real-time environmental data. This data is then combined with a **pre-existing agriculture dataset** to improve model robustness and prediction accuracy. ML algorithms analyze the merged dataset to provide actionable recommendations for farmers.

---

## ⚙️ Features

* Real-time monitoring of **temperature, humidity, and soil moisture**
* Wireless data transmission from **Arduino-based sensor nodes**
* **IoT integration** for data storage and visualization
* **Hybrid dataset**: combination of real-world Arduino data + pre-existing dataset
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

## 📊 Dataset

* **Arduino Sensor Data** → Real-time values of temperature, humidity, and soil moisture.
* **Pre-existing Dataset** → Agricultural dataset (sourced externally, e.g., Kaggle).
* **Combined Dataset** → Both datasets were merged to create a larger, more diverse dataset for training and testing.

  * Ensures more **robust ML models**
  * Improves **accuracy of irrigation scheduling and crop yield predictions**

---

## 📊 Workflow

1. **Data Collection:** Sensors collect temperature, humidity, and soil moisture values.
2. **Data Integration:** Arduino-collected data combined with pre-existing dataset.
3. **Data Storage:** Data stored locally/cloud for ML training.
4. **Preprocessing:** Cleaning, scaling, and merging using Pandas.
5. **Machine Learning Models:**

   * **KNN / Random Forest / SVM** → irrigation & crop recommendations
   * **Decision Tree** → interpretable rule-based suggestions
   * **K-Means** → clustering soil conditions
6. **Recommendation System:** Suggests when & how much to irrigate for improved crop yield.

---


---

## 🚀 How to Run

### Arduino

1. Upload code from `Arduino_Code/agrisense.ino` to Arduino Uno.
2. Connect DHT11 & Soil Moisture sensor as per pin configuration.

### Machine Learning

```bash
# Install dependencies
pip install -r requirements.txt
```

* Run any ML notebook in `ML_Models/` to train models.
* Example (Random Forest):

```python
from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier()
model.fit(X_train, y_train)
print("Accuracy:", model.score(X_test, y_test))
```


---

## 📈 Results

* **Arduino-only dataset** → Baseline accuracy (smaller dataset, limited variability)
* **Pre-existing dataset** → Larger dataset, more general patterns
* **Combined dataset** → Best accuracy and recommendations (Random Forest performed highest ~90%)
* Irrigation scheduling optimized → **reduced water usage** and **improved yield prediction**

---

## 📌 Future Enhancements

* Add **fertilizer recommendation system**
* Deploy ML models on **TinyML (Arduino Nano 33 BLE)** for edge inference
* Build a **web/mobile dashboard** for farmers



👉 Do you want me to also **prepare a sample `combined_dataset.csv`** (with dummy values for temp, humidity, moisture) so your repo looks complete even if people don’t have your Arduino hardware?
