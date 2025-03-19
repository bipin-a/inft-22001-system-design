# **Assignment 2: Designing and Deploying a Machine Learning API**

## **Objective**
Develop and deploy a machine learning application as an API that addresses a specific prediction task. You will demonstrate your understanding of the full development lifecycle, from model selection to API deployment.

## **Overview**
You will:
1. Develop an ML model for a chosen prediction task.
2. Evaluate and document its performance.
3. Deploy it as an API service.
4. Define user interaction and data contracts.
5. Monitor and measure API performance.
6. Present your work in a video demonstration.

## **Assignment Breakdown**

### **1. Select a Prediction Task**
Choose one of the following ML tasks for your API:
- **Text Summarization**
- **Question Answering**
- **Translation**
- **Risk Modeling** (with `predict_proba`)
- **Forecasting** (using time series cross-validation)

### **2. Select a Dataset**
Choose a dataset that aligns with your task. Suggested datasets:
- **Forecasting**: `m4_weekly` dataset (`load_dataset("autogluon/chronos_datasets", "m4_weekly")`)
- **Risk Modeling**: [Company Bankruptcy Prediction dataset](https://www.kaggle.com/datasets/fedesoriano/company-bankruptcy-prediction/data)
- **NLP Tasks**: Consider using pre-trained models like ["sentence-transformers/all-MiniLM-L6-v2"](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2).

**Note:** If you would like to use a different dataset, please message me so I can approve or provide an alternative. 

### **3. Define Your API’s Users**
Clearly specify:
- **Target users** (who are the clients?)
- **Expected daily request volume** (How many requests per day)
- **User requirements** (e.g., real-time responses, batch processing?)

### **4. Model Development**
- Select an appropriate algorithm (e.g., XGBoost, CatBoost, Logistic Regression, SVM).
- Document why you chose this model.
- Evaluate model performance using suitable metrics (e.g., F1-score, RMSE, Log Loss).

> **Reminder**: Accuracy is a horrible metric.

### **5. API Service Performance**
Monitor and document:
- **Response time** (processing duration per request)
- **Memory consumption** (minimum and maximum usage)
- **Cloud monitoring dashboards** (number of expected requests)

### **6. User Interaction**
Define how users will interact with the API:
- **Input format**: Textbox, file upload?
- **Output format**: Graph (Plotly/Seaborn), text box, JSON?

### **7. Data Contract Specification**
Use **Pydantic** to define:
- **Input data validation** (types, constraints, required fields)
- **Response structure** (expected output format)

### **8. Deployment**
- **Containerization**: Use **Docker**.
- **Cloud Deployment**: Choose **Cloud Run (GCP)** or **AWS Lambda**. (GCP has a free tier, and AWS too)
- **Documentation**: Clearly outline the deployment steps and configurations.

## **Bonus Points (Optional Enhancements)**
- **Implement a Population Stability Index (PSI)** for feature drift analysis of the features between train, test and OOS.
- **SHAP Value Visualization** (beeswarm plots for feature importance).

---

## **Submission Guidelines**
### **1. Code Submission (GitHub Repo)**
Your repository must include:
- **README** with clear setup instructions. The Users definition should be in your read me. Along with a diagram explaining how someone interacts with your service.
- **API documentation** (auto-generated via `docs/` endpoint).
- **Code for model training, API, and deployment scripts**.

### **2. Video Submission (50% of Grade)**
Create a **clear, structured** video presentation:
- **Face cam required** (use OBS Studio or Microsoft Teams).
- **Explain your architecture** (use diagrams from the readme and walk me through the code).
- **Show API demonstration** (`docs/` endpoint walkthrough).
- **Model Training Explained** (Walk me through how you trained your model).
- **Model Service Explained** (Walk me through how you served your model).
- **Max length: 10 minutes** (points deducted for exceeding).

**🚫 Do NOT read directly from a script.** It must be a natural explanation (as if you were presenting in front of the class).

---


## **Important Constraints**
- **No frontend required** – focus on backend API.
- **Demonstrate API functionality using `docs/` endpoint**.
- **Keep video under 10 minutes** – strict time limit.
