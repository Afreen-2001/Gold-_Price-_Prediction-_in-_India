Gold Price Prediction in India 🇮🇳
📌 Project Overview

This project is a Machine Learning-based web application that predicts the price of 1 gram of gold in India using a trained regression model. The application is built using Python and Gradio, providing a simple and interactive user interface.

Users can enter the USD/INR exchange rate, and the application uses a pre-trained regression model to predict the gold price.

Note: This application provides a model-based prediction and does not fetch real-time gold prices or exchange rates automatically.

🚀 Features
Predicts the price of 1 gram of gold in India.
Uses a trained regression model for prediction.
Applies feature scaling using a pre-trained scaler.
Provides an interactive web interface using Gradio.
Displays predictions rounded to two decimal places.
Can generate a publicly accessible sharing link using Gradio.
🛠️ Technologies Used
Python – Programming language
NumPy – Numerical computations and input processing
Scikit-learn – Model preprocessing and prediction support
Pickle – Loading the saved model and scaler
Gradio – Building the interactive web application
📂 Project Structure
Gold-Price-Prediction/
│
├── app.py             # Main Gradio application
├── regressor.pkl      # Trained regression model
├── scaler.pkl         # Fitted feature scaler
├── requirements.txt   # Project dependencies
└── README.md          # Project documentation

⚙️ Installation and Setup
1. Clone the repository
git clone https://github.com/Afreen-2001/Gold-_Price-_Prediction-_in-_India.git


Navigate to the project directory:

cd YOUR_REPOSITORY

2. Create a virtual environment (optional)
python -m venv venv


Activate the environment.

Windows:

venv\Scripts\activate


macOS/Linux:

source venv/bin/activate

3. Install dependencies
pip install gradio numpy scikit-learn


Alternatively, install the packages listed in requirements.txt:

pip install -r requirements.txt


Ensure that the scikit-learn version is compatible with the version used to save the model and scaler.

4. Run the application
python app.py


Gradio will provide a local URL, typically:

http://127.0.0.1:7860


Open the URL in your browser to use the application.

🧠 How It Works
The trained regression model and fitted scaler are loaded from the .pkl files.
The user enters a USD/INR exchange rate.
The input is converted into a NumPy array.
The scaler transforms the input into the format expected by the model.
The regression model predicts the gold price.
The predicted value is rounded to two decimal places and displayed in the interface.
💻 Code Example
def calculate_goldrate(usd_inr):
    scaled_input = scaler.transform(
        np.array(usd_inr).reshape(1, -1)
    )
    prediction = model.predict(scaled_input)[0]
    return round(float(prediction), 2)

📊 Model and Data

The application uses a pre-trained regression model stored in regressor.pkl and a fitted scaler stored in scaler.pkl.

The prediction accuracy depends on the quality of the training data, the selected features, and the performance of the trained model.

The input must match the feature or features used during model training. The model and scaler files must be available in the expected directory.

🌐 Sharing the Application

The application uses:

demo.launch(share=True)


This allows Gradio to generate a temporary public URL that can be shared with other users. The URL is not intended as permanent hosting.

For a persistent deployment, consider hosting the application on Hugging Face Spaces or another suitable cloud platform.

⚠️ Limitations
The application does not retrieve live gold prices.
The application does not automatically retrieve the current USD/INR exchange rate.
Predictions depend on the trained model and its input features.
Actual gold prices vary with market conditions, purity, taxes, and location.
The predicted price should not be treated as a guaranteed market price or financial advice.
🔮 Future Improvements
Integrate a live gold-price API.
Fetch current USD/INR exchange rates automatically.
Display historical gold-price trends using charts.
Add support for different gold purities, such as 22K and 24K.
Evaluate and display model performance metrics.
Deploy the application as a permanent web service.
👨‍💻 Author

Your Name

GitHub: https://github.com/YOUR_USERNAME
📄 License

This project is intended for educational and demonstration purposes. Add a license file to specify the terms under which others may use, modify, and distribute the project.

⭐ If you find this project useful, consider giving the repository a star!