# cyber-fraud-detection-project
Bank fraud detection using Machine Learning
Attending International Conference on Emerging Technologies and its Application (ICETA -2026)


Abstract
With the increasing adoption of online banking and digital transactions, the risk of bank fraud has risen significantly. Fraudulent transactions can cause substantial financial losses to both banks and their customers. Therefore, a fast and accurate fraud detection system is essential.This project presents a Bank Fraud Detection System using machine learning techniques. The system analyzes transaction dataincluding transaction amount, time, location, and customer activityto identify suspicious transactions. By learning from historical transaction records, the machine learning model recognizes patterns and differentiates between genuine and fraudulent transactions. This approach reduces manual effort and financial losses while improving customer security and detection accuracy.The system helps prevent unauthorized transactions and creates a safer banking environment. The main objective is to enhance banking security, reduce financial losses, and protect customer accounts from unauthorized activities. The proposed system enables banks to monitor transactions more effectively and take timely action against potential fraud.Machine learning provides a smart and efficient way to detect fraud, improving the reliability of digital banking services. Successful implementation of this system can increase customer trust and contribute to a safer banking environment. Additionally, machine learning makes the system more intelligent and capable of adapting to new fraud patterns.
Keywords: Bank Fraud Detection, Machine Learning, Digital Banking Security, Transaction Analysis, Anomaly Detection, Financial Fraud Prevention.
 
1.INTRODUCTION
Bank fraud is an issue these days. When you do your banking online use your card at a store, take out cash from an ATM, or make a payment on your phone, there is always a chance that someone will try to cheat you.This kind of thing can happen in a lot of ways. It usually results in big money losses for both the bank and the people who have accounts there [1].Bank fraud can happen when you are shopping online or when you are at a store. Because of this, banks really need to have a system that can find fraud quickly and get it right every time [2].Having this kind of system is very important for banks now [3].Bank fraud is a problem and banks need to stop it.
•	ABOUT THE PROJECT DETAILS
This project is about a system that helps detect fraud at banks. The system looks at information about transactions like how much money's moved, when and where it happens, and what the customer normally does[4]. It uses this information to find transactions that do not seem right. The system gets better at finding fraud by looking at transactions. Over time, it can tell what a transaction is and what is a fake one. The bank fraud detection system uses machine learning techniques to make this happen. The machine learning model learns from transaction records and gets good at recognizing patterns so it can tell the difference between real transactions and bank fraud[5].
•	CORE ADVANTAGE 
The main advantage of this approach is that it saves us a lot of work and helps us avoid losing money. This approach also makes our customers safer by finding transactions that are not allowed across all the ways we do banking. Not just when we bank online[6]. The system stops transactions that are not allowed and makes the whole banking environment a safer place for this approach. This approach really helps because it finds these transactions and this approach makes banking safer for everyone using this approach.
 
 
 
•	CURRENT FRAUD DETAILS FROM RESERVE BANK OF INDIA 
According to data available from the Reserve Bank of India , the fourth quarter ended March 2023 itself witnessed payment frauds of over Rs 800 crore under the new format of fraud reporting.
    These findings should be concerning   or bank managers across the country. While the amount may not seem significant as compared to the volume of transactions, it reveals vulnerabilities in banks’ anti-fraud mechanisms.
Caption: Number of bank fraud cases across India from FY 2009 – 2022
 Source :Increased adoption of digital payments and digitalisation of the financial ecosystem has led to the rise of identity theft and cybercrime .
In this piece, we’ve put together a guide on the common types of frauds and how banks can detect and combat them effectively.


2.LITERATURE REVIEW
Bank fraud detection has become an important area of research because the increasing use of online banking, digital payments, and credit card transactions has led to a rise in fraudulent activities. Researchers have explored various machine learning techniques to identify fraudulent activities and reduce financial losses. [1].Traditional rule-based fraud detection systems are often ineffective against evolving fraud patterns, leading researchers to adopt Machine Learning (ML) techniques for improved detection accuracy[5].Researchers have therefore focused on machine learning techniques that can automatically learn from historical transaction data and accurately identify suspicious activities.Many researchers have found that machine learning algorithms like Logistic Regression, Decision Trees, Random Forest, SVM, and XGBoost can help detect fraud. Among these, Random Forest often gives better results and higher accuracy. Researchers alsosay that cleaning the data is very important before training the model. This includes filling missing values, removing duplicate records, and balancing the data using techniques like SMOTE and undersampling.
 
  Findings from Existing Literature
  Several recurring findings emerge across studies:
 
•	Finding 1: Machine learning significantly outperforms traditional rule-based systems.
•	Finding 2: Data preprocessing greatly affects model performance.
•	Finding 3: Class imbalance remains the most challenging issue.
•	Finding 4: Ensemble methods such as Random Forest and XGBoost consistently achieve superior results.
•	Finding 5: Feature engineering improves detection accuracy substantially.
•	Finding 6: Combining multiple models often produces better fraud detection rates than single-model approaches.
Although previous studies have achieved promising results, challenges such as class imbalance, evolving fraud patterns, data privacy concerns, and real-time detection remain significant. Therefore, further research is required to develop more robust and adaptive banking fraud detection systems using advanced machine learning techniques.

3.METHODOLOGY
Step 1: Data Collection
The first step was to get the data needed for training the model. A banking transaction dataset was should be downloaded from Kaggle, which is a well-known website for finding datasets. The dataset contains real-world transaction information including transaction amount, transaction type, sender balance before and after the transaction, receiver balance before and after the transaction, and a fraud label which tells whether the transaction was Real or fraudulent. Having this label is very important because the machine learning model needs examples of both real and fraudulent transactions to learn from.

Step 2: Data Preprocessing
Once the data was collected, it needed to be cleaned. Real-world data is mostly messy, so this step took some time. First, the dataset was checked for missing values. Any missing values were either removed or filled with appropriate numbers. Second, columns that were not useful for fraud detection, like transaction ID or step numbers  were removed so the model wouldn't get confused by extra information. Third, categorical data such like transaction type (PAYMENT, TRANSFER, CASHOUT) was converted into numbers because machine learning algorithms only understand numbers. After these steps, the data is clean and ready for analysis.
 
Step 3: Exploratory Data Analysis 
Before building the model, it is always fair to explore the data and understand what it seems. This is called Exploratory Data Analysis (EDA). Python libraries like Pandas, NumPy, Matplotlib, and Seaborn were used for this purpose. Various charts and graphs were created to see patterns. For example, bar charts were made to see how many fraudulent transactions existed compared to real ones. Histograms were structured to see the distribution of transaction amounts. Heatmaps were used to understand relationships between different features. Through this analysis, it became clear that fraudulent transactions are very rare compared to genuine ones. This is called an imbalanced dataset, and it is a usual challenge in fraud detection
.                  

Step 4: Feature Selection
After exploring the data, the next step was to decide which features would get used to train the model. Not all features are equally useful. Based on the EDA results, the following features were selected as input variables:
•	Transaction Type (payment, transfer, cash-out, etc.)
•	Transaction Amount (how much money was involved)
•	Old Balance of Sender (sender's balance before transaction)
•	New Balance of Sender (sender's balance after transaction)
•	Old Balance of Receiver (receiver's balance before transaction)
•	New Balance of Receiver (receiver's balance after transaction)
These features were chosen because they directly relate to how money moves. When fraud happens, these balances often change in unusual ways. The fraud label was kept separate because that is what the model needs to predict it is not used as an input feature.
Step 5: Model Training
Once the features were selected, it was time to train the machine learning model. The dataset was first split into two parts: 80% for training and 20% for testing. The training part was used to teach the model, and the testing part was kept aside to check how well the model performs on data it has never seen before.
The algorithm used for this project was Random Forest. Random Forest is a popular choice for fraud detection because it is accurate and handles complex patterns well. It works by creating many decision trees and then combining their results to make a final prediction. During training, the model learned to associate certain patterns with fraud. For example, it might learn that when a large amount is transferred to a new receiver and the sender's balance drops to nearly zero, that transaction is likely to be fraud. The model learned these patterns automatically from the historical data. 
Step 6: Model Evaluation
After training, the model needed to be tested to see how well it actually works. The testing set (20% of the data) was used for this purpose. Several performance metrics were calculated: Accuracy tells the percentage of total predictions that were correct.
Precision tells, out of all transactions flagged as fraud, how many were actually fraud.
Recall tells, out of all actual fraudulent transactions, how many were caught by the model.
Confusion Matrix shows the four outcomes: true positives (correctly caught fraud), true negatives (correctly identified genuine), false positives (genuine flagged as fraud), and false negatives (fraud missed).For fraud detection, recall is very important. It is better to have some false alarms than to miss a real fraud. The results showed that the Random Forest model performed well, catching most fraudulent transactions while keeping false alarms at a reasonable level.
Step 7: Deployment
The final step was to make the model usable. A machine learning model sitting in a notebook is not helpful for a bank. So the trained model was deployed into a web application using Streamlit, a Python library that makes it easy to build simple web apps.
The web application works like this: A user opens the app in a browser, enters transaction details like amount, transaction type, and balances, and clicks a "Predict" button. Behind the scenes, the app passes the inputs through the trained model and shows the result either "Fraudulent Transaction Detected" or "Transaction Appears Genuine." This app can be run locally or deployed to the cloud for real use.


Tools and Technologies Used: 
The following tools were used in this project:
Tool						Purpose
1.	Python					Main programming language
2.	SQL					Storing and querying data
3.	Pandas, NumPy			Dataprocessing and manipulation
4.	Matplotlib, Seaborn			Creating visualizations
5.	Scikit-Learn				Machine learning (Random Forest)
6.	Streamlit				Building the web app
7.	Jupyter Notebook / VS Code		Writing and testing code

All of these tools are free and open-source.
Source 1 :
Figure 1: df["type"].value_counts().plot(kind="bar",title="transaction types",color ="skyblue")
plt.xlabel("transaction type")
plt.ylabel("count")
plt.show

                           
Source 2:  
fraud_by_type = df.groupby("type")["isFraud"].mean().sort_values(ascending=False)
fraud_by_type.plot(kind="bar",title="fraud rate by type",color="salmon")
plt.ylabel("fraud rate")
plt.show()
                           
Souce 3 :   
sns.histplot(np.log1p(df["amount"]),bins=100,kde = True, color="green")
plt.title("transaction Amount Distribution (log scale)")
plt.xlabel("log(Amount + 1 )")
plt.show()

#graph 2 

sns.boxenplot(data= df[df["amount"]<50000], x = "isFraud",y="amount")
plt.title("Amount vs isFraud (Filtered under 50k)")
plt.show()
  
Source 4 :
frauds_per_step = df[df["isFraud"] ==1]["step"].value_counts().sort_index()
plt.plot(frauds_per_step.index , frauds_per_step.values, label="Frauds per step")
plt.xlabel("step (Time)")
plt.ylabel("Number of Frauds")
plt.title("Frauds Over Time")
plt.grid(True)
plt.show()

#graph 2 

sns.countplot(data=fraud_types,x="type",hue="isFraud")
plt.title("Fraud Distribution in  Transfer & Cash_Out")
plt.show()

# graph 3 

sns.heatmap(corr,annot=True,cmap ="coolwarm",fmt=".2f")
plt.title("Correlation Matrix")
plt.show()

# graph 4 

Pipeline = Pipeline([
("prep",preprocessor),
("clf",LogisticRegression(class_weight="balanced",max_iter=1000))

])

  

   
 
Expected Outcome :
When fully implemented, this system is expected to bring several benefits. It will detect fraud fasterin milliseconds instead of hours or days. It will minmize manual effort because only suspicious transactions need human review. It will improve transaction security and minimize financial losses by catching fraud before money is stolen. Most importantly, it will increase customer trust in digital banking. When customers know that an intelligent system is watching their transactions, they feel safer. Banks that adopt such systems will be better protected, and their customers will be more confident in using digital banking services

1.	RESULTS AND DISCUSSION 
The machine learning models were trained and tested using a bank transaction dataset to classify transactions as either fraudulent or legitimate. Three algorithms were evaluated: Logistic Regression, Decision Tree, and Random Forest.
The performance of the models is summarized below:
Algorithm			Accuracy
    Logistic Regression		93%
    Decision Tree		95%
    Random Forest		99%
 
Among all the models, the Random Forest algorithm achieved the highest accuracy of 99%, making it the most effective model for detecting fraudulent transactions. The Decision Tree model also performed well with an accuracy of 95%, while Logistic Regression achieved 93% accuracy.
 
The results of this study show that machine learning techniques are highly effective for detecting fraudulent banking transactions. Different models were tested, and their performance was compared to understand which algorithm works best for fraud detection.Logistic Regression provided a basic and stable performance, but it was less effective in handling complex transaction patterns. Decision Tree improved the detection capability by learning rules from the dataset; however, it sometimes suffered from overfitting, especially with large data. Random Forest performed the best among all models.
steamlit run fraud_detection.py
              
 
 CONCLUSIONS
In this research, a machine learning-based system for detecting bank fraud has been successfully studied and analysed. The main objective was to identify fraudulent transactions accurately and improve the security of banking systems.
 
Different machine learning algorithms such as Logistic Regression, Decision Tree, and Random Forest were used and compared. The results show that Random Forest performed the best with the highest accuracy of 99%, making it the most effective model for fraud detection.

 
Overall, the proposed system helps in reducing financial losses, improving customer trust, and enhancing the security of digital banking systems. Future improvements can include the use of deep learning models and real-time fraud detection systems for even better performance.
 
 

