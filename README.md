### **Alphabet Soup Funding Success Prediction**

**Overview of the Analysis:**  
The goal of this project is to create a binary classification model to predict whether an organization funded by Alphabet Soup will be successful. Using TensorFlow, I designed, trained, and evaluated a neural network to meet this goal.

---

### **Results**

#### **Data Preprocessing**

- **What variable(s) are the target(s) for your model?**  
  The target variable is `IS_SUCCESSFUL`, which indicates whether funding was used effectively.  

- **What variable(s) are the features for your model?**  
  Features include `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, and `ASK_AMT`.  

- **What variable(s) should be removed from the input data because they are neither targets nor features?**  
  The `EIN` and `NAME` columns were removed because they do not provide meaningful information for the model.  

---

#### **Compiling, Training, and Evaluating the Model**

- **How many neurons, layers, and activation functions did you select for your neural network model, and why?**  
  The model included 3 hidden layers with increasing numbers of neurons (e.g., 128, 64, 32). The first two layers used the ReLU activation function to capture non-linear patterns, while the output layer used Sigmoid for binary classification. This structure was chosen to balance model complexity and predictive performance.  

- **Were you able to achieve the target model performance?**  
  Yes, the model achieved an accuracy of over 75%, meeting the performance goal.  

- **What steps did you take in your attempts to increase model performance?**  
  - Required converting the NAME into data points which has the biggest impact on improving efficiency
  - Added a third hidden layer to improve the model's ability to learn complex patterns.  
  - Fine-tuned hyperparameters like the number of neurons and activation functions.  

---

### **Summary of Results**  
The final model achieved an accuracy of over 75%, correctly classifying the test data with a high degree of reliability. Key features that influenced success included certain application types, classifications, and funding requests.

---

### **Recommendation**  
An alternative approach could use a **Gradient Boosting Machine (GBM)**, such as XGBoost or LightGBM. These models are well-suited for structured data and handle categorical variables effectively with less preprocessing. They work by building smaller models iteratively, improving accuracy over time while being computationally efficient. This approach might simplify the workflow and still achieve high accuracy.  
