# deep-learning-challenge
Homework for Module 21- Neural Networks and Deep Learning


For this project, we are using a csv provided by non-profit company "Alphabet Soup" containing funding data for over 34,000 organizations that we are using to train a binary classier to predict whether applicants will be successful if provided funding.

**Data Preprocessing**
* **Target Variable** - We are using the IS_SUCCESSFUL column from our dataset as the target variable. This indicates if the funding money was used effectively.
* **Feature Variables**
    * APPLICATION_TYPE - Alphabet Soup application type
    * AFFILIATION - Affiliated sector of industry
    * CLASSIFICATION - Government organization classification
    * USE_CASE - Use case for funding
    * ORGANIZATION - Organization type
    * INCOME_AMT - Income classification
    * ASK_AMT - Funding amount requested
* **Variables Removed**
    * EIN and Name were initially removed due to their values being used for identification purposes and not providing predictive value.
    * Additionally, we removed STATUS and SPECIAL_CONSIDERATIONS due to the highly imbalanced/skewed data which would not contribute predictive value for our model.

* **Compiling, Training, and Evaluating the Model**
    * For the final model, I used 3 hidden layers with 95 neurons, 55 neurons, and 15 neurons respectively. Multiple training passes were performed with different amounts of layers and neurons in each layer, but after experimenting with these changes we settled on this structure after noticing a performance plateau with our model.
    * I was not able to achieve target model performance of 75%, coming close with an overall accuracy of 73%. Various methods were used attempting to achive the target performance value but overcoming that proved challenging.
    * In my attempts to improve the performance of the model, I added additional neurons and layers to the model, dropped additional values from the feature set, adjusted the learning rate of the model, experimented with dropout layers to determine if overfitting was an issue, tested different activation functions such as relu and tanh, and adjusted scaling methods for our ASK_AMT feature.

**Summary**
My deep learning model achieved a reasonable accuracy of 73% when attempting to predict successful funding applicants. Although multiple optimization methods were attempted to increase the accuracy of the model, ultimately the performance appeared to plateau and did not improve much. I would recommend exploring different models such as a Random Forest or XGBoost model to test their ability to solve our classification problem. These methods can prove effective with handling categorical data such as what we are provided for this project and can provide insight into feature importance which may show which features provide better predictive value for our classification problem.