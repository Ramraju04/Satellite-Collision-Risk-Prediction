# 🚀 Satellite & Space Object Collision Risk Prediction

## Overview

Satellite collisions and space debris have become major challenges in modern space operations. With thousands of active satellites and millions of debris fragments orbiting Earth, predicting potential collision events is critical for mission safety and sustainability.

This project presents a **Machine Learning-based Collision Risk Prediction System** that estimates the severity or risk of potential collisions between satellites and space objects using orbital dynamics and encounter-related parameters.

The system is implemented as an interactive web application using **Streamlit** and utilizes a trained **Random Forest Regression Model** for prediction.

---

## Problem Statement

As the density of objects in Earth's orbit increases, collision avoidance has become an important aspect of satellite operations.

Traditional approaches often rely on physics-based simulations and computationally expensive calculations. This project explores the use of Machine Learning to estimate collision risk using historical orbital encounter features.

The objective is to:

- Analyze orbital encounter parameters
- Predict collision severity/risk score
- Provide a user-friendly prediction interface
- Demonstrate Machine Learning applications in aerospace analytics

---

## Key Features

### Machine Learning Prediction Engine
- Trained Random Forest Regression Model
- Fast prediction generation
- Handles nonlinear orbital relationships

### Interactive Streamlit Dashboard
- User-friendly web interface
- Real-time prediction results
- Easy parameter input

### Input Validation
- Controlled numerical ranges
- Prevents invalid orbital values
- Improves prediction reliability

### Preloaded Sample Data
- Default values available for testing
- Allows quick demonstration

### Collision Risk Assessment
- Generates a collision risk score
- Higher scores indicate higher collision severity

---

## Technology Stack

| Component | Technology |
|------------|-------------|
| Programming Language | Python |
| Frontend | Streamlit |
| Machine Learning | Scikit-Learn |
| Data Processing | Pandas |
| Numerical Computation | NumPy |
| Model Serialization | Joblib |

---

## Project Architecture

```
User Inputs
      │
      ▼
Input Validation
      │
      ▼
Feature Processing
      │
      ▼
Random Forest Model
      │
      ▼
Risk Prediction
      │
      ▼
Results Dashboard
```

---

## Project Structure

```
Asteroid-Collision-Prediction/
│
├── CollisionPrediction.py
├── DisplayConstraints.py
├── WithConstraints.py
├── random_forest_model.pkl
├── requirements.txt
├── README.md
└── LICENSE
```

### File Description

#### CollisionPrediction.py

Basic implementation of the prediction system with predefined satellite encounter parameters.

#### DisplayConstraints.py

Enhanced version that displays detailed information about every input parameter and their valid ranges.

#### WithConstraints.py

Advanced implementation with:

- Input validation
- Constraint enforcement
- Risk interpretation
- Enhanced user experience

#### random_forest_model.pkl

Serialized Random Forest machine learning model used for collision risk prediction.

---

## Input Parameters

The model utilizes multiple orbital and encounter-related features.

### Orbital Parameters

| Parameter | Description |
|------------|-------------|
| t_j2k_sma | Target object semi-major axis |
| t_j2k_ecc | Target object eccentricity |
| c_j2k_sma | Chaser object semi-major axis |
| c_j2k_inc | Chaser object inclination |

### Relative Motion Parameters

| Parameter | Description |
|------------|-------------|
| relative_speed | Relative speed |
| relative_velocity_t | Tangential velocity |
| relative_velocity_n | Normal velocity |

### Orbital Heights

| Parameter | Description |
|------------|-------------|
| t_h_apo | Apogee height |
| t_h_per | Perigee height |
| c_h_per | Chaser perigee height |

### Positional Parameters

| Parameter | Description |
|------------|-------------|
| geocentric_latitude | Geocentric latitude |
| azimuth | Orbital azimuth angle |

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/Asteroid-Collision-Prediction.git
cd Asteroid-Collision-Prediction
```

### Create Virtual Environment

Windows

```bash
python -m venv venv
venv\Scripts\activate
```

Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Dependencies

```txt
streamlit
pandas
numpy
joblib
scikit-learn
```

---

## Running the Application

### Basic Version

```bash
streamlit run CollisionPrediction.py
```

### Version with Input Constraints

```bash
streamlit run WithConstraints.py
```

### Full Constraints Dashboard

```bash
streamlit run DisplayConstraints.py
```

---

## Example Workflow

### Step 1

Launch the application.

### Step 2

Enter orbital encounter parameters.

### Step 3

Click **Predict**.

### Step 4

The trained Random Forest model evaluates the input features.

### Step 5

A collision risk score is generated and displayed.

---

## Machine Learning Model

### Algorithm

Random Forest Regression

### Why Random Forest?

- Handles nonlinear relationships
- Reduces overfitting
- Works effectively with structured tabular data
- Provides strong predictive performance

### Prediction Output

The model predicts a numerical collision risk score.

Interpretation:

| Score | Risk Level |
|---------|------------|
| Low | Minimal collision risk |
| Moderate | Requires monitoring |
| High | Potential collision threat |
| Very High | Immediate attention required |

---

## Applications

This system can be useful for:

- Satellite collision monitoring
- Space debris analysis
- Aerospace research
- Machine Learning demonstrations
- Educational purposes
- Orbital safety studies

---

## Future Improvements

### Data Improvements

- Larger orbital datasets
- Real-world conjunction data
- Historical collision events

### Model Improvements

- XGBoost
- LightGBM
- Deep Neural Networks

### Visualization

- Orbit visualization
- Risk heatmaps
- Interactive dashboards

### Deployment

- Docker support
- AWS deployment
- Azure deployment
- Kubernetes deployment

---

## Results

The application successfully predicts collision risk scores based on orbital encounter parameters and demonstrates the feasibility of applying Machine Learning techniques to aerospace safety analysis.

---

## License

This project is licensed under the MIT License.

---

## Author

### Ramraju

AI/ML Engineer | Python Developer | Generative AI Enthusiast

GitHub: https://github.com/Ramraju04

LinkedIn: Add Your LinkedIn URL

---

## Acknowledgements

- Streamlit Team
- Scikit-Learn Community
- Open Source Python Ecosystem
- Aerospace Research Community

---

⭐ If you found this project useful, consider starring the repository.
