# Doctor-s-Fees-Prediction-
Predicting doctor's fees understanding their basic information

In this time we all need doctors at any time for check-up or in any emergency. But   we find that their wages or consultancy fees are too high also for a well-settled individual. Some charges are very high and some very low but have a clinic in remote area. What if we can correlate their wages with other valuable information of the doctor and build a machine learning model that can predict the fees? Let’s go ahead and find that.


### Data Information:
Here we have gathered 2 datasets having the important information of the doctors and one of them having the fees also.
The features are as follows:
i.	**Qualification**:    The degrees and diplomas of the doctor.
ii.	**Experience**:  experience in practice (years).
iii.	**Rating**:  rating given by the patients (in %).
iv.	**Place**:  The residence of the clinic.
v.	**Profile**:   Speciality of the doctor.
vi.	**Miscellaneous Info**: Other important information.
#### Datasets has been taken from-   https://kaggle.com/nitin194/doctor-fees-prediction
#### This project can be found in kaggle- https://www.kaggle.com/sagnik1511/doctor-s-fee-prediction-using-random-forest





### Brief Approach:
We have partitioned the whole project into several small steps.
1.	**Libraries**: We need different libraries in python to get the job done.

2.	**Data Gathering and Primary Visualization**: In this step we are turning the excel f iles into pandas data frame for visualization in Jupyter Notebook and for further processing. Visualizing the data can help us process the data in a particular manner.

3.	**Pre-processing**:  In this step we have to process the data into a suitable format for model fitting and prediction.  This step is divided into other small steps. In this project we have all the data in object format. So, we had to process new features from the features in the data, derive the numerical values from the string attributes. We also had to fill the leakages as per their usability in the data. 

4.	**EDA (Exploratory Data Analysis)**: After preparation of data we need to visualize the data to understand the correlation between the features. So, we can find any feature as not valuable / misleading the prediction and delete it.

5.	**Encoding**: After finding suitable features for prediction we have to change all the categorical columns into numerical features as the models only runs on numbers. So, we had three columns ‘Area’, ‘City’, ‘Profile’ which needed to be encoded.

6.	**X  and Y generation** : As this is a type of supervised machine learning problem , we have to split the target feature from the main dataset which is ‘fees’.

7.	**Model Generation and Fitting**: As we have the X and Y, we used a random forest based regression classifier named ‘RandomForestRgressor’. On training over the model we have achieved an accuracy of 88% on train data.

8.	**Evaluation Metric**: we have used the RMSE metric for evaluation. We found that model provides 64.42 RMSE value. So , we created a validation for checking the bias in the model and found that the model is not overfitting which is a good signal.

9.	**Output Generation**: After creating a well tuned model we predicted the test data with the model and generated a .csv file as an output. The output contains an id number along with predicted fees of the doctors which are in decimal representation.
