# 📊 Telecom Customer Churn Prediction

## 📌 Project Overview

Telecom Customer Churn Prediction is a Machine Learning project that predicts whether a telecom customer is likely to leave the service or continue using it.
The project analyzes customer information such as tenure, contract type, monthly charges, internet services, payment methods, and other service-related features to identify customers who may be at risk of churning.
An interactive web application built using **Streamlit** allows users to enter customer details and receive a churn prediction along with the estimated churn probability.

## 🎯 Objectives

- Predict whether a customer is likely to churn.
- Analyze customer characteristics associated with churn.
- Apply and evaluate multiple classification algorithms.
- Address class imbalance using SMOTE.
- Build an interactive application for real-time predictions.

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Imbalanced Data Handling:** SMOTE (Imbalanced-learn)
- **Model Persistence:** Joblib
- **Web Application:** Streamlit
- **Development Environment:** Jupyter Notebook, VS Code

## 📂 Project Structure

```text
Telecom-Churn-Prediction/
│
├── app.py
├── Classification  model.ipynb
├── churn_model.pkl
├── scaler.pkl
├── requirements.txt
└── README.md
```

**Note:** The dataset used for training should also be included if its license permits redistribution. The trained model and scaler files are required to run the current application.

## 📊 Dataset Description

The project uses telecom customer data containing customer demographics, service subscriptions, billing information, contract details, and the churn target.

Key features include:

- Gender and senior citizen status
- Partner and dependents
- Customer tenure
- Phone and internet services
- Online security and device protection
- Technical support and streaming services
- Contract type and payment method
- Monthly charges and total charges
- **Target variable:** Churn — whether the customer left the service

## ⚙️ Project Workflow

1. **Data Collection:** Load the telecom customer dataset.
2. **Data Preprocessing:** Inspect missing values, prepare features, and encode categorical variables.
3. **Exploratory Data Analysis (EDA):** Examine customer churn distribution and customer characteristics.
4. **Train-Test Split:** Divide the dataset into training and testing sets.
5. **Class Imbalance Handling:** Apply SMOTE to balance the training data.
6. **Model Building:** Train and compare classification algorithms, including Logistic Regression, Decision Tree, Random Forest, SVM, and boosting models.
7. **Hyperparameter Tuning:** Use GridSearchCV to optimize model parameters.
8. **Model Evaluation:** Evaluate model performance using accuracy, precision, recall, F1-score, confusion matrix, and ROC-AUC where calculated.
9. **Deployment:** Integrate the saved model with a Streamlit web application.

## 🤖 Machine Learning Model

The saved model in this project is a **Random Forest classifier selected through GridSearchCV**, using the best estimator from the Random Forest pipeline.

The pipeline includes:

- MinMaxScaler for feature scaling
- SMOTE for handling class imbalance during training
- Random Forest for classification

The Streamlit application accepts customer details, prepares the input features, and displays the predicted churn class and churn probability.

## 📈 Model Performance

On the held-out test set, the tuned Random Forest model achieved the following results in the notebook:

| Evaluation Metric | Score |
|---|---:|
| Accuracy | 78.44% |
| Precision — Churn | 58.15% |
| Recall — Churn | 73.87% |
| F1-score — Churn | 64.97% |

These values are calculated from the notebook's confusion matrix. They represent the reported test-set results and are not a guarantee of performance on new customer data.

**Why recall matters:** Higher churn recall means the model identifies a larger proportion of customers who actually leave, helping a telecom company prioritize customer retention efforts.

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/Telecom-Churn-Prediction.git
```

### 2. Open the project folder

```bash
cd Telecom-Churn-Prediction
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Streamlit application

```bash
python -m streamlit run app.py
```

### 5. Use the application

- Open the local URL displayed in your terminal, usually `http://localhost:8501`.
- Enter the customer's information in the sidebar.
- Click **Predict Churn**.
- View the predicted customer status and estimated churn probability.

## 📦 Requirements

Create a `requirements.txt` file with the following packages:

```text
streamlit
pandas
numpy
scikit-learn
imbalanced-learn
joblib
matplotlib
seaborn
```

The visualization libraries are needed if you plan to run the notebook's EDA and plotting cells. The Streamlit app itself uses a smaller subset.

## 💡 Key Learnings

- Data cleaning and preprocessing
- Exploratory Data Analysis
- Encoding categorical variables
- Handling imbalanced datasets using SMOTE
- Training and evaluating classification models
- Hyperparameter tuning using GridSearchCV
- Saving and loading machine learning models with Joblib
- Deploying a machine learning model using Streamlit

## 🔮 Future Improvements

- Add interactive EDA charts to the application.
- Improve model performance through further experimentation.
- Add feature importance and explainable AI visualizations.
- Deploy the application to a cloud hosting platform.
- Provide actionable customer retention recommendations.

## 👨‍💻 Author

**Shreyash Chavan**

- LinkedIn: [Add your LinkedIn profile URL]
- GitHub: [Add your GitHub profile URL]

---

⭐ If you find this project interesting, feel free to star the repository!
