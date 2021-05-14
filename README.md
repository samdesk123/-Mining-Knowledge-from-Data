# Mining-Knowledge-from-Data
# Introduction
- The main purpose of the data set’s recording is to be able to model the rotor temperatures of a permanent magnet synchronous motor (PMSM) in real-time. Due to the intricate structure of an electric traction drive, direct measurement with thermal sensors is not possible for rotor temperatures, and even in case of the stator temperatures, sensor outage or even just deterioration can’t be ad- ministered properly without redundant modeling. In addition, precise thermal modeling gets more and more important with the rising relevance of functional safety.
- Your task is to design a model with appropriate feature engineering, that esti- mates one target temperature rotor temperature (“pm”) in a causal manner. In order to maintain real-time capability, model sizes should be as small as possi- ble, while retain a high level of prediction accuracy, as temperature estimation in production will be deployed on best-cost hardware of traction drives in an au- tomotive environment, where lean computation and lightweight implementation is key and crucial.
Specifically, the problem you are going to solve is: Can you:
  - accurately predict the rotor temperature given the collected data with a model the size of which is as small as possible?
  - well explain your prediction and the associated findings? For example, identify the key factors are strongly associated with the response variable, i.e., rotor temperature.
# Data Set
- The data set contains 15,147 instances, each of which have 13 columns: the first 8 columns corresponding to the attributes (e.g., ambient, coolant, u d, u q, motor speed, torque, i d, i q) and the 9th column “pm” containing the rotor temperature, i.e., the variable that we will predict. The details of the data set can be found in the original Kaggle competition. It is a good idea to read the detailed description before do this assignment.
- The dataset used in this assessment is generated based on the full dataset with a reduced size. Therefore, please download the data set from Moodle. You are not allowed to use the original dataset available on the Kaggle website. Please note that the three original target features “stator yoke”, “stator winding” and “stator tooth” should not be used.
- In order to do evaluate the generalizability of your model, you will need to use samples from profile id. 72 and 81 for testing, the rest is for training.


# Prediction task

- For the prediction task, the underlying problem is to predict the rotor tempera- ture using the collected 8 attributes. The provided data sets are well organised, you do not need to wrangle the data. However, please make sure you understand the intuition of these attributes.
- To measure the performance of your model(s), you firstly split the original data into training and testing set (profile id. 72 and 81), fit the model using the training set, do the prediction on the test set and compute some performance metrics.
In this task, in addition to the final model, you are also required to
  1. compare at least one model that is di↵erent from your final model, 
  2. describe and justify the choice of your models,
  3. assess, analyze and interpret your results

# Inference task
The purpose of the inference task is to identify the key factors that have strong a↵ect on the rotor temperature. In other words, which property contributes the most to your model’s performance? Inference can be based on variable correlation analysis, regression equations, or any other form. The descriptions and the accompanying interpretation must be comprehensible, useful and with statistic support whenever it is possible. To finish this task, you should use proper data analysis techniques to
  1. identify a subset of attributes that have a significant impact on the pre- diction of the burned area;
  2. report your identification with statistical evidence (e.g. correlations, p- values) and interpret the identified attribute subset (e.g. as to why certain attributes have certain impacts on the prediction).
