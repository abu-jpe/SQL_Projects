# Credit Card Fraud Detection (SQL + Python)

This project analyzes anonymized credit card transaction data to identify fraudulent activity using both SQL and Python-based techniques. It includes schema creation, SQL queries, and exploratory data analysis with visualizations to highlight behavioral patterns associated with fraud.

## 📌 Background

Credit card fraud causes billions in losses globally. In this project, I analyze two days of transaction data — focusing on abnormal behavior, time-based clustering, and outlier detection. While machine learning is often used to combat fraud, strong data analysis using SQL and Python remains foundational to understanding patterns and flagging anomalies.

## 🧠 Dataset

- **Source**: [Kaggle – Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- 284,807 transactions made by European cardholders over two days in 2013
- 492 transactions labeled as fraud (only 0.172%)
- PCA-transformed features (`V1` to `V28`) + `Time`, `Amount`, and `Class`

## 📂 Project Structure
<pre lang="text"><code>
.
├── schema.sql                 # Table creation script (PostgreSQL)
├── creditcard.csv            # Anonymized raw transaction data
├── queries.sql               # SQL-based fraud queries
├── notebooks/
│   └── challenge.ipynb        # Python notebook for visualization
├── images/
│   ├── early_hour.png
│   ├── id_holder_2.png
│   ├── id_holder_18.png
│   └── anomalous_transaction.png
└── README.md                 # Project overview and documentation
</code></pre>


---

## 🧱 Data Preparation

The dataset was loaded into a PostgreSQL database after defining a normalized relational schema. Primary and foreign key constraints were used to mimic real-world structure. I also generated an ERD to understand the relationships between key variables before performing SQL analysis.

> Note: Dataset source was anonymized and PCA-transformed; features include `Time`, `Amount`, and principal components `V1–V28`.

---

## 📊 Data Analysis

Analysis was conducted using both SQL and Python. SQL was used to filter, aggregate, and flag transactions of interest. Python was used to visualize the output and identify patterns.

Key tasks:
- Querying the top 100 transactions between 7:00 AM and 9:00 AM to assess fraud risk during that period
- Identifying micro-transactions (e.g., <$2.00) often used to test stolen cards
- Detecting outliers using boxplots and statistical analysis
- Visualizing fraudulent transactions across time

> 📓 Full code and visualizations: [challenge.ipynb](challenge.ipynb)

---

## 💡 Key Observations

- Fraudulent transactions tend to include both very small and very large amounts
- Certain hours of the day (e.g., early morning) had elevated fraud activity
- Outliers were detected using both IQR and standard deviation techniques
- Micro-transactions may indicate card testing by bad actors

---

## 🛠️ Tools Used

- PostgreSQL  
- SQL  
- Python (`pandas`, `seaborn`, `matplotlib`)  
- Jupyter Notebooks  

---

## 🧠 What I Learned

This project helped sharpen my ability to:
- Design and implement relational database schemas
- Clean and manipulate financial data in SQL
- Communicate findings visually using Python
- Investigate fraud behavior using real-world assumptions

---

## 🚀 Future Work

- Integrate machine learning techniques (logistic regression, XGBoost) to predict fraud probability  
- Add a dashboard layer (e.g., Streamlit or Tableau) for stakeholder reporting  
- Explore adversarial approaches to test the robustness of fraud rules  

---

## 📬 Contact

If you'd like to discuss this project or others like it, feel free to reach out via GitHub or [LinkedIn](https://www.linkedin.com/in/promiseabu/).
