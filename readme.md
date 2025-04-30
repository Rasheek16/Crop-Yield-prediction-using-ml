

## 🌾 Crop Yield Prediction using Weather and Vegetation Data

This project aims to predict **crop yield (kg/ha)** based on environmental factors such as temperature, precipitation, humidity, and vegetation index using a deep learning model built with Keras.

---

### 📁 Dataset Description

The synthetic dataset used in this project was generated from a real-world agricultural dataset with the following features:

| Feature      | Description                                |
|--------------|--------------------------------------------|
| `T2M`        | Average air temperature (°C)               |
| `PRECIP`     | Precipitation (mm)                         |
| `RH2M`       | Relative humidity at 2 meters (%)          |
| `NDVI`       | Normalized Difference Vegetation Index     |
| `yield_kg_per_ha` | Crop yield (kg per hectare) — target variable |

> The dataset includes 1000 synthetic samples generated using PCA and interpolation from real trends, to maintain realistic variability and feature correlation.

---

### ⚙️ Model Architecture

The model is a **fully connected feedforward neural network** built using TensorFlow/Keras:

- Input Layer: 4 neurons (T2M, PRECIP, RH2M, NDVI)
- Hidden Layer 1: 128 neurons, ReLU
- Hidden Layer 2: 64 neurons, ReLU
- Hidden Layer 3: 32 neurons, ReLU
- Output Layer: 1 neuron (yield), Linear activation

**Loss Function**: Mean Squared Error (MSE)  
**Optimizer**: Adam (learning rate = 0.001)

---

### 🧪 Data Splits

- **Training set**: 60%  
- **Validation set**: 20%  
- **Test set**: 20%

All input features are standardized using `StandardScaler`.

---

### 🔁 Callbacks Used

- `EarlyStopping`: Stops training if validation loss doesn't improve for 20 epochs.
- `ModelCheckpoint`: Saves the model with the lowest validation loss (`best_model.h5`).

---

### 📊 Model Performance

After training:

- **MAE**: 0.37 kg/ha  
- **R² Score**: 1.0

> (Replace with actual numbers after training)

---

### 📈 Training History Plot

A training and validation loss plot is generated to visualize model learning behavior.

---



