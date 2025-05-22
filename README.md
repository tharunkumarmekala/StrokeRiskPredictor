
# Stroke Risk Predictor

This repository contains the full source code, pretrained models, and web application for a stroke risk prediction system built using machine learning techniques, primarily XGBoost and ensemble methods. The system provides real-time stroke risk assessment based on clinical and demographic inputs collected via a user-friendly web interface.


## Features

- **User-friendly Frontend:** Input form with dropdown menus for easy selection of clinical and demographic variables.
- **Backend Analysis:** Python Flask server processes inputs and generates stroke risk predictions using pretrained models.
- **Dynamic Output:** Real-time display of personalized stroke risk scores and health recommendations.
- **Model Explainability:** Feature importance analysis provides clinical interpretability.
- **Optimized Threshold:** Improved sensitivity for stroke detection through threshold tuning.
- **Ensemble Modeling:** Combines XGBoost, Random Forest, and Gradient Boosting for enhanced robustness.


## Repository Contents

- `app.py` — Flask backend server handling requests and running predictions.
- `index.html` — Frontend web interface with dropdown input options.
- `models/` — Pretrained machine learning model files saved with joblib.
- `Dataset.csv` — Stroke dataset used for training and evaluation.
- `screenshots/` — Images demonstrating the input interface and dynamic output display.
- `requirements.txt` — Python dependencies for running the application.

## Setup and Usage

1. **Clone the repository:**

   ```bash
   git clone https://github.com/tharunkumarmekala/StrokeRiskPredictor.git
   cd StrokeRiskPredictor
   ```

2. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Flask app:**

   ```bash
   python app.py
   ```

4. **Access the web interface:**

   Open your browser and navigate to `http://localhost:5000`

5. **Input data using the dropdown menus, submit, and view real-time stroke risk prediction and recommendations.**

---

## Dataset

The dataset used for training the models is included in the `data/` directory. It contains clinical and demographic features relevant to stroke risk prediction.


## Screenshots

Two key screenshots demonstrating the system workflow are included in the `screenshots/` folder:

- Input form with dropdown selections for clinical variables.
- Dynamic display showing the predicted stroke risk and personalized recommendations after backend processing.

These illustrate the smooth and practical user experience from data entry to results visualization.

![image](https://github.com/user-attachments/assets/063f4195-e278-4592-8b86-08dab7a8b6c8)


## License

This project is open source and available under the [MIT License](LICENSE).


## Contact

For questions or contributions, please contact:

Tharun Kumar Mekala  
Email: [tharunkumar39429@gmail.com]  
GitHub: [https://github.com/tharunkumarmekala](https://github.com/tharunkumarmekala)


Thank you for exploring this stroke risk prediction system.
