📊 Customer Lifetime Value (CLV) Prediction using Regression

📌 Project Overview
Customer Lifetime Value (CLV) represents the total revenue a business can expect from a customer over the entire relationship period.
This project focuses on predicting CLV using regression models based on customer demographics, transaction behavior, engagement, and satisfaction data.

The goal is to build an interpretable, leakage-free, and production-ready regression pipeline.

📁 Dataset
Rows 7,000 customers
Features 20 (demographics, transactions, engagement, satisfaction)
Target Variable LTV (log-transformed for modeling)

🧠 Problem Statement
Predict the Customer Lifetime Value of users to help businesses
Identify high-value customers
Improve retention strategies
Optimize marketing and resource allocation

🔍 Exploratory Data Analysis (EDA)
Identified right-skewed distribution in LTV
Applied log transformation to stabilize variance
Detected and removed data leakage features
Analyzed numeric and categorical features using 
Histograms
Scatter plots
Box plots
Correlation heatmap

🛠️ Data Preprocessing
✔️ Feature Engineering
Removed data leakage columns (e.g., Total_Spent)
Removed redundant features causing multicollinearity
Log-transformed target variable (LTV_log)

✔️ Encoding
Label Encoding (ordinal)
Income_Level
App_Usage_Frequency

One-Hot Encoding (nominal)
Location
Preferred_Payment_Method

✔️ Scaling
Applied StandardScaler on numeric features
Prevented data leakage by fitting scaler only on training data

🤖 Models Used
The following regression models were trained and compared

Model	Description
Linear Regression	Baseline model
Ridge Regression	L2 regularization for stability
Lasso Regression	L1 regularization + feature selection

📈 Model Performance
Model	R² Score
Linear Regression	~0.817
Ridge Regression	~0.817
Lasso Regression	~0.817 (Best)

✔️ Lasso Regression was selected as the final model because
Comparable or slightly better performance
Automatic feature selection
Better interpretability
Reduced overfitting risk

🔑 Key Insights
Transaction behavior and customer satisfaction are the primary drivers of CLV
Demographic and location-based features have limited direct impact
Proper preprocessing and leakage handling significantly improve model reliability

🧪 Technologies Used

Python
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
Google Colab
Git & GitHub

📌 Future Improvements
Hyperparameter tuning using cross-validation
Residual analysis and assumption checks
Deployment as a REST API
Experimenting with tree-based ensemble models

👤 Author
Prajwal S
B.Tech Student 

⭐ How to Use
Clone the repository
Open the notebook in Jupyter  Colab
Run cells sequentially to reproduce results

⭐ If you found this project useful, feel free to star the repository!
