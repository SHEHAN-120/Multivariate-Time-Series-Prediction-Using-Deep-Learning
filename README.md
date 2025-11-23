# ⚡ Energy Consumption Prediction (LSTM)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge\&logo=python\&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.0%2B-orange?style=for-the-badge\&logo=tensorflow\&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge\&logo=visual-studio-code\&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-green?style=for-the-badge)

A Deep Learning project to predict household appliance energy consumption based on environmental sensor data (Temperature, Humidity, Weather) using **Long Short-Term Memory (LSTM)** networks.

---

## 📂 Project Structure

```bash
├── data/
│   ├── raw/                # Original CSV dataset
├── models/                 # (Empty / Placeholder folder)
├── src/                    # Source code and Working Directory
│   ├── models/             # 📂 Saved Model Files
│   │   ├── trained_model.h5  # Final trained LSTM model
│   │   ├── best_model.h5     # Checkpoint (Lowest validation loss)
│   │   └── scaler.pkl        # Saved MinMaxScaler for inference
│   ├── ab.ipynb            # Feature Engineering modules
│   ├── data_preprocessing.ipynb # Cleaning and Scaling logic
│   ├── model.ipynb         # LSTM Architecture definition
│   ├── train.ipynb         # Main training notebook
│   └── predictions.ipynb   # 🔮 Inference Notebook (Run this here)
├── reports/                # PDF Documentation and Figures
├── README.md               # Project Documentation
└── requirements.txt        # Python dependencies
```

---

## 🛠 Tech Stack

* Python 3.10.0
* TensorFlow 2.0+
* Scikit-learn
* Jupyter Notebooks
* VS Code

---

## ⚙️ Installation & Setup (Important!)

Before running any code, you must create a virtual environment and install the required libraries to avoid conflicts.

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/energy-prediction-lstm.git
cd energy-prediction-lstm
```

### 2. Create Virtual Environment

```bash
# Windows
python -m venv venv

# Mac / Linux
python3 -m venv venv
```

### 3. Activate the Environment

```bash
# Windows
.\venv\Scripts\activate


You will know it is activated when you see **(venv)** at the start of your terminal line.

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

## 🚀 How to Run

Since the source files are Jupyter Notebooks (`.ipynb`), use **VS Code** or **Jupyter Lab**.

### 🔹 Step 1: Train the Model

1. Open VS Code.
2. Navigate to `src/` and open `train.ipynb`.
3. Ensure your kernel is set to `venv` (top right corner).
4. Click **Run All**.

This will clean the data, train the LSTM, and save `trained_model.h5` inside `src/models/`.

### 🔹 Step 2: Run Inference (Predictions)

1. Open `src/predictions.ipynb`.
2. Click **Run All**.
3. Scroll to the bottom to see the output:

```plaintext
PREDICTION RESULT
Predicted Consumption: 296.44 Wh
```

---

## 📊 Model Performance

The model was evaluated using **RMSE** and **MAE** metrics on the test set (20% split).

| Metric   | Score                |
| -------- | -------------------- |
| RMSE     | *0.1010* |
| MAE      | *0.0676*  |
| R2 Score | *0.6312*   |

---
