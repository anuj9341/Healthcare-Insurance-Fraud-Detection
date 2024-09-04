# Healthcare-Insurance-Fraud-Detection

Note: Unable to add Train_Outpatientdata.csv as the file is more than 25mb.

Project on Machine Learning

link to the dataset: https://www.kaggle.com/datasets/rohitrox/healthcare-provider-fraud-detection-analysis

Dataset consists of 8 files(4 train,4 test).

The Inpatient data(with 40,474 records, 30 features) and Outpatient data(with 5,17,737 records, 27 features) consisted of many missing values so, for both scenarios features with more than 50% missing values were dropped.

Rest of missing values were imputed with KNN(For missing numerical values) and Random imputation(For missing catergorical values) methodology.

The beneficiary data is combined with Inpatient data ,Out patient separately and then the target data is combined to have two datasets to work on.

The Inpatient had shape of 40,474 records, 44 features and Outpatient had shape of 5,17,737 records, 32 features.

In those new datasets , Random Forest (as a feature selector) is applied to get the importance score for all the features.

For Inpatient dataset the threshold of 0.04 is and for out patient dataset threshold of 0.02 is set respectively.

Now a two new datasets derived by this feature selection methodology. So for Inpatient data the shape is (40,747,6) and for Outpatient dataset the shape is (517737,12).

The datasets have been standardized utilizing the StandardScaler module.

The dataset underwent division into training and testing subsets, followed by the application of oversampling and under sampling techniques.

The resultant dataset was employed to train Random Forest Classifier and Decision Tree Classifier models, which were subsequently evaluated using performance metrics including F1-score and the area under the ROC curve (AUC).
