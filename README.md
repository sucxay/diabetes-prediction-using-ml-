🧠 Diabetes Prediction API using FastAPI

A Machine Learning API built with FastAPI that predicts whether a patient is diabetic based on selected medical features.

This project demonstrates how to move a model from a notebook into a production-ready backend that can be connected to any frontend (React, Angular, Web Apps, Mobile Apps).

🚀 Features

✅ Trained ML model using selected dataset columns only
✅ High-performance FastAPI backend
✅ Ready for frontend integration
✅ Interactive Swagger UI
✅ Clean project structure
✅ Beginner-friendly production ML example

📊 Model Features Used

The model is trained strictly on the following columns:

dataset.iloc[:, [1,4,5,7]].values

Which correspond to:

Glucose

Insulin

BMI

Age

⚠️ Important:
The prediction request must follow the SAME feature order.

🏗️ Project Structure
project/
│
├── main.py          # FastAPI application
├── model.pkl        # Trained ML model
├── diabetes.csv     # Dataset
└── README.md
⚙️ Installation
1️⃣ Clone the repository
git clone <your-repo-url>
cd project
2️⃣ Create Virtual Environment (Recommended)
python -m venv venv

Activate:

Mac/Linux

source venv/bin/activate

Windows

venv\Scripts\activate
3️⃣ Install Dependencies
pip install fastapi uvicorn scikit-learn pandas numpy
▶️ Running the API

Start the server:

uvicorn main:app --reload

Server will run at:

http://127.0.0.1:8000
📘 Interactive API Docs

FastAPI automatically generates Swagger documentation:

http://127.0.0.1:8000/docs

You can test predictions directly from the browser 🔥

🔮 Prediction Endpoint
POST /predict
Request Body:
{
  "Glucose": 130,
  "Insulin": 80,
  "BMI": 32.5,
  "Age": 45
}
Response:
{
  "prediction": 1,
  "result": "Diabetic"
}
🧪 Training the Model

If you want to retrain the model:

Update the training script

Save the model again as:

model.pkl

⚠️ Never change feature order unless you retrain the model.

💡 Why This Project Matters

This is NOT just a notebook project.

It demonstrates real-world ML workflow:

👉 Train model
👉 Serialize model
👉 Serve via API
👉 Connect to frontend
👉 Deploy

These are the skills companies expect from production-ready ML engineers.

🔥 Future Improvements

Dockerize the API

Deploy on AWS / Render

Add authentication

Build React frontend

Implement model versioning

Add CI/CD

👨‍💻 Tech Stack

Python

Scikit-learn

FastAPI

Uvicorn

NumPy

Pandas

⭐ If you like this project

Give it a star ⭐ on GitHub — it helps others find it!