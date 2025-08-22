<h1 style="color:#D32F2F;">Enhancing Healthcare with AI: Transformer Models for Prediction in Maternal Health</h1>

<h2 style="color:#1976D2;">Introduction</h2>  
Maternal mortality remains a critical public health issue in rural India, largely due to limited healthcare access and the absence of early warning systems. Traditional rule-based methods often lacked real-time predictive capabilities.  

In this project, I developed an explainable AI model to predict maternal health risks using demographic and clinical data. The focus was on achieving both high prediction accuracy and interpretability using SHAP values to build trust among healthcare workers. The work specifically addressed three research questions: whether deep learning can outperform traditional machine learning in maternal risk prediction, which features are most predictive of maternal complications, and how SHAP can improve trust in AI-driven decisions.  

<h2 style="color:#1976D2;">Methodology</h2>  
The dataset was obtained from the Open Government Data Platform (India), consisting of approximately 30,000 records and 24 features. Features included maternal age, delivery history, awareness of HIV/RTI, and knowledge of danger signs. The target variable was outcome_pregnancy, which had three classes: no risk, cannot decide, and complication.  

Preprocessing steps included imputing missing values, dropping irrelevant columns, encoding categorical variables using label encoding, and addressing class imbalance through stratified sampling.  

Three models were implemented and compared. Logistic Regression served as the baseline. Random Forest was used to explore feature importance. A Tab-Transformer model was developed as a deep learning approach leveraging self-attention for tabular data.  

For explainability, SHAP (SHapley Additive exPlanations) was applied to interpret predictions and provide transparency into model decisions.  

<h2 style="color:#1976D2;">Results</h2>  
The Logistic Regression model achieved an accuracy of 84.58 percent with a weighted F1-score of 83.25 percent. Random Forest performed slightly better with 85.96 percent accuracy and an F1-score of 84.50 percent. The Tab-Transformer achieved the best validation accuracy of 86.73 percent.  

The results showed that the most predictive features included maternal age, delivery history, and awareness of danger signs. The Tab-Transformer outperformed traditional models by capturing complex feature interactions more effectively. SHAP analysis further revealed nonlinear relationships, such as certain age thresholds that significantly influenced the likelihood of high-risk pregnancies.  

<h2 style="color:#1976D2;">Challenges and Solutions</h2>  
The dataset presented challenges in terms of missing values and irrelevant features, which were addressed through careful imputation and feature removal. Class imbalance was mitigated using stratified sampling to ensure fair representation of all classes. To address the challenge of interpretability, SHAP was integrated to generate actionable insights for healthcare workers, thereby bridging the gap between AI predictions and practical healthcare decision-making.  

<h2 style="color:#1976D2;">Future Work</h2>  
Future extensions of this work include testing the models on datasets from different regions of India to enhance generalizability. Another planned improvement is real-time deployment by integrating the models into mobile applications for rural healthcare workers. Additionally, hybrid approaches that combine the Tab-Transformer with temporal models such as LSTMs can be explored to analyze longitudinal maternal health data more effectively.  

<h2 style="color:#1976D2;">Impact</h2>  
The models developed in this project demonstrate significant clinical utility by enabling early intervention through AI-driven risk stratification. The use of SHAP ensures interpretability and builds trust among non-technical healthcare providers. Furthermore, lightweight models such as Random Forest provide scalability for low-resource settings, making this work practical for real-world applications in rural healthcare.  

<h2 style="color:#1976D2;">Tech Stack</h2>  
This project was implemented in Python using libraries such as Pandas, NumPy, Scikit-learn, and PyTorch. Deep learning was carried out using the Tab-Transformer architecture. SHAP was employed for explainability, and visualizations were created using Matplotlib and Seaborn.  

