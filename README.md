### **Alphabet Soup Funding Success Prediction**

**Overview of the Analysis:**  
The goal of this analysis is to create a binary classification model using machine learning to predict whether an organization funded by Alphabet Soup will be successful. Using TensorFlow, I designed, compiled, trained, and evaluated a neural network model to achieve this goal.

---

### **Results**

#### **Data Preprocessing**
- **Target Variable:** `IS_SUCCESSFUL` (indicates funding success).  
- **Features:**  
  - `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, and `ASK_AMT`.  
- **Removed Columns:**  
  - `EIN` (Employee Identification Number) and `NAME` (not beneficial for predictions).  

#### **Model Compilation, Training, and Evaluation**
- **Neural Network Details:**  
  - **Structure:** 3 hidden layers.  
  - **Neurons per Layer:** Increasing neurons in each layer to improve accuracy.  
  - **Activation Functions:** ReLU for the first two layers; Sigmoid for the output.  
- **Performance Achieved:**  
  - Accuracy exceeded 75%, meeting the target.  

#### **Optimization Steps:**
- Encoded categorical variables using `pd.get_dummies`.  
- Added a third hidden layer to improve accuracy.  
- Utilized activation functions (ReLU and Sigmoid) to enhance performance.  

---

### **Summary of Results**
- The final model achieved an accuracy of over 75%, correctly classifying test data with reasonable confidence.  
- Key predictors of success include high-frequency application types and specific classifications, along with other influential features.

---

### **Recommendation**
Another way to solve this problem could be to use a **Gradient Boosting Machine (GBM)**, like XGBoost or LightGBM. These models are good at finding patterns in data and can improve accuracy by learning from mistakes made in earlier steps. They also work well with structured data and don’t need as much preparation for categorical information. This makes them a simpler and more efficient choice for this kind of task.
