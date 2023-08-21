# Predicting Bail Status and Bail Amount

**Author:** Snigdha Panakanti

**Term:** Summer 2023

Presentation Link:
https://github.com/SnigdhaPanakanti/Panakanti_data606/blob/99a51421966d36cebed0aabc72bf544676b5be38/doc/BAIL%20STATUS%20AND%20AMOUNT%20PREDICTION.pptx

YouTube Link: ---link---

## Introduction:

Most people rarely think about arraignment or bail. This topic usually requires a specific impetus to be considered. One may need to learn about bail till they or a friend is arraigned. An individual is arraigned after being arrested. The prosecutor and defense discuss the arrest and the defendant's criminal history. They also discuss bail conditions. After that, the judge decides whether to grant bail, the amount, and non-monetary conditions. The court's final say on bail raises questions about its fairness. Many factors can impact a judge's decision. The type of offense is usually the main factor in bail. Consider whether gender and ethnicity affect bond amounts. Why does time matter? How long did the judge sleep last night? Is a judge unbiased enough to set fair and effective bail? 

Malcolm Gladwell also questions judicial bail decisions in Talking to Strangers (2019). Malcolm references a study by economist Sendhil Mullainathan and computer scientists. The researchers developed an artificial intelligence system using New York City's 2008–2013 data on defendants' ages and criminal records. This technology generated a list of bail-eligible defendants so they may await trial at home. Gladwell's (2019) study found that AI-generated lists reduced the risk of people committing crimes while waiting for trial by 25%. 

The AI system also created a risk distribution framework to classify defendants as low, moderate, or high. Gladwell (2019) found that judges granted bail to people across the spectrum. This study shows that bail determination is random, prompting a comparison of human and automated bail-setting methods. 

The present study examines New York State pre-trial data (Division of Technology & Court Research, 2022), a comprehensive dataset on criminal case apprehension and initial court procedures. This study examines gender, race, and bail settings. Next, prediction models will estimate bail likelihood, amount, and non-monetary restrictions. These prediction algorithms allow defendants and their families to submit their information before arraignment to estimate the bail amount. 

## Issue of Interest:

Machine learning has improved bail in previous studies. More oversight is needed for judges seeking bond assistance. Judges must evaluate each case to determine bail. Case-specific differences complicate the work. Thus, judges may need help weighing their options. Research reveals that environmental influences affect judicial outcomes. A study indicated that judges were 65% likely to grant parole at the start of the day but 0% later. Judges' parole approval rates recovered to 65% after a break (Kleiner, 2011). Decision fatigue causes this tendency. Decision fatigue occurs when people tire of making multiple judgments and rely on basic responses that may not fully assess the facts (Kleiner, 2011). 

The PSA program influenced bail rulings for Kentucky judges. The algorithmically determined dangerousness measure helped judges grant bail to more people. More minority criminals received bail than in similar instances (Covert, 2020). During this time, 13% more defendants were released on recognizance without posting bail or other non-monetary obligations (Covert, 2020). However, judges no longer examine PSA bail discrepancies (Covert, 2020). Covert (2020) found that judges gave Black defendants cash bail higher than intermediate risk estimations. The assessment was helpful. Lack of a fixed address affects defendants' risk estimates regardless of violation, according to Covert (2020). This judgment is based on their likely absence from court (Covert, 2020). 

The idea that those without addresses cannot appear in court is not widespread. Some people without permanent residence attend court under the Bail Project (Covert, 2020). Additionally, risk assessments may need to be more meaningful. Covert's (2020) study indicated that 99% of Cook County, Illinois, high-risk offenders released on bail did not face violent offense charges until trial. 

Public safety, judicial efficiency, and individual and communal welfare are addressed when setting bail. It takes work for adjudicators to measure the benefits of some against the risks of the whole population. Sometimes, using machine learning algorithms to decide certain cases increases justice. The method may unintentionally foster social inequality and systematic prejudice. We aim to construct a bail determination model that properly mimics judicial decision-making without bias. 

## Goal of the Project:

This study aims to investigate two distinct facets of the dataset. The primary objective is to thoroughly analyze the dataset to investigate the potential association between race and bail amounts, as well as gender and bail amounts. The primary objective of this research is to develop three distinct prediction models. These models aim to forecast 1) the likelihood of bail being established and 2) the specific amount of bail that will be set. The objective of the prediction models is to develop an interface that allows individuals to input various personal details, such as age, gender, race, charge, charge severity, prior criminal acts, and other relevant information, to generate a prediction for their bond amount. 

## Data Source and Data Attributes:

The dataset utilized for the analysis was sourced from the New York State Unified Court System. The dataset comprises criminal arraignments at the state level, with updates occurring semi-annually to incorporate new cases and revise earlier extracts. Within this dataset, multiple columns furnish comprehensive information about the charges brought against individuals and the corresponding court proceedings that ultimately determine whether the charges are upheld or dismissed. The collection encompasses information gathered within the vicinity of New York City, comprising an estimated total of 63 courts. The decisions regarding the release of individuals at arraignment may differ across different courts, and the specific details about these choices have been duly recorded in the data. The dataset is categorized into several columns to conduct hypotheses based on the provided information. The primary variables utilized in the dataset for all hypotheses include Gender, Race, Ethnicity, Age of crime and arrest, Arraign Charge Category, Representation Type in the court, Release Decision at Arraign, Bail Amount, and Arrest Type. The dataset's overall size is 194MB, stored in the .csv file format, with 284,096 rows and 108 columns. 

Source link: https://ww2.nycourts.gov/pretrial-release-data-33136 

## Data Analysis and Visualizations:

Firstly, the dataset is distributed and analyzed to determine the bail outcomes. And before building the Machine Learning Model on the tidy dataset, the correlation between different features/factors and Bail status is analyzed. The seaborne library is used to plot the ages of criminals, revealing that most offenders fall between the ages of 25 and 35. The bail amount is allocated based on arraignment charge categories and displayed in a bar plot. And before building the Machine Learning Model on the tidy dataset, the correlation between different features/factors and Bail amount is analyzed. The dataset is distributed and analyzed to determine the bail amount based upon the Top charge severity at arrest. 

![image](https://github.com/SnigdhaPanakanti/Panakanti_data606/blob/e642ee84fb0c965f533daed31ac3b278cba400dc/Data/images/overview.png)
![image](https://github.com/SnigdhaPanakanti/Panakanti_data606/blob/e642ee84fb0c965f533daed31ac3b278cba400dc/Data/images/top10.png)
![image](https://github.com/SnigdhaPanakanti/Panakanti_data606/blob/8c15cdf4e1dbc9d7dc0216d8172e8619bba74b69/Data/images/demographics.png)
![image](https://github.com/SnigdhaPanakanti/Panakanti_data606/blob/993cc77b4190b7b12266dfdf63e5b8a8b6e7625d/Data/images/severity_at_arrest.png)

## Modelling:
### Predicting Bail Status

This study employed three models, each utilizing a distinct approach to test the initial hypothesis. The findings of all three models will be compared, and the model that best fits the data will be fine-tuned to enhance the accuracy of the results. 

1. Baseline Model:
   The training process of the dataset was initiated with the utilization of the Dummy Classifier, which employs straightforward rules to generate predictions. This model was constructed as a foundational reference point to compare its outcomes with other models.
   Our model has achieved a baseline accuracy of 71.18%, which cannot be surpassed by any other model. 

2. Logistic Regression:
   The logistic regression algorithm, which falls under supervised learning classification algorithms, is employed to estimate the probability of a target variable. Logistic regression is the most effective approach when the target variable is categorical.  

       Accuracy Score: 72.5% 

       Precision Score: 73.94% 

       F1 Score: 83.03% 

The Logistic regression model demonstrates an accuracy rate of 72.5%, surpassing that of the baseline model. Furthermore, our precision value indicates the accuracy in predicting favorable outcomes within the dataset. 

3. Gaussian Naive Bayes Model:
The Gaussian Naïve Bayes model is a probabilistic classifier that assumes the features are independent and normally distributed. The Naive Bayes algorithm is a straightforward approach for constructing classifiers, which are models designed to assign class labels to issue situations represented as feature vectors. These class labels are chosen from a finite range of options. Based on the labeled training and test data provided, the model yielded the following outcomes. 

        Accuracy Score:71.04% 
        Precision Score: 74.11% 
        F1 Score: 81.73% 

The accuracy score got from the Gaussian Naïve Bayes is less than the Logistic Regression Model. Also, the F1 score is less than the Logistic regression model.

4. K-Nearest Neighbours (KNN) Model:
The K-Nearest Neighbours (KNN) algorithm is utilized for the classification of new data points. This is achieved by identifying the K-Nearest Neighbors from the training dataset and determining the class of the new data point based on the majority class among its neighbors. The model was assigned a k-value of 7 for the purpose of training and testing our data, resulting in the following output. 

        Accuracy Score: 76.39% 
        Precision Score: 79.67% 
        F1 Score: 84.38% 

The K-nearest neighbors (KNN) method has demonstrated superior accuracy compared to the aforementioned models. The Precision score exhibited a significant rise compared to other models' scores. In order to improve the outcomes, we shall adjust the parameters. 

Model Comparision:

As we have created different models, we will compare their results using graphs to determine the best fit for our dataset. We will use two charts - one to compare the predicted scores of the models and the other to compare the ROC curves. 

![image](https://github.com/SnigdhaPanakanti/Panakanti_data606/blob/99a51421966d36cebed0aabc72bf544676b5be38/Data/images/Model_Comparision.png)

From the above chart, we can say that the K-NN algorithm is the best fitting model for our dataset except for the Recall value. So, we will choose the K-NN model further to tune the parameter to obtain better scores and predictions. 
In the K-NN algorithm, we have tuned the n_neighbors value to 5 and found that the model provides better results compared to previous results. 

    Accuracy: 0.7736451207922186
    F1 Score: 0.8486474612439592
    Precision: 0.8090650710545999
    Recall: 0.8923021084237965
Further, have modified the split of the dataset into testing and training as 20% and 80% respectively. Fed the model with the new test and train dataset and the model provided a great accuracy score, F-1 score, and precision score above 80%. 

    Accuracy: 0.8284582893347413
    F1 Score: 0.8819761457891868
    Precision: 0.8635210432720806
    Recall: 0.9012373174956694

### Predicting Bail Amount
Here, I have conducted four regression analyses using various algorithms to test the hypotheses. To preprocess the model, we remove dummy values and some extra features from the dataset such as 'Age_at_Crime', 'Age_at_Arrest', 'Judge_Name', 'Arrest_Type', 'Top_Charge_at_Arrest,’ Violent_Felony_Ind', 'Representation_Type',"Top_Charge_at_Arrest", "Top_Charge_Weight_at_Arrest", 'Release Decision at Arraign', 'Year.' 
The columns 'Age','Def_Attended_Sched_Pretrials',"prior_vfo_cnt", "prior_nonvfo_cnt", "prior_misd_cnt" were scaled to model the model-feeder. To finish up the data pre-processing to provide input to the models, we will split the dataset into two datasets training and testing data. Here, we have divided the dataset as 30% and 70% for Testing and Training, respectively. 

1. Linear Regression Model:
Two linear regression models were performed: one with prior offenses and one without. The metrics for each model are listed below. 

  Model 1: 
    
    Features: Crime, Race, Gender, Prior offenses, Age, Pretrials attended, Court ORI 
    R2: -8.362228404040309e+19 
    MSE: 6.950283441536962e+18 

  Model 2: 

    Features: Crime, Race, Gender, Court ORI 
    R2: -3.042231583411607e+21 
    MSE: 2.4994588369169252e+20 

Decision Regression Model: 

Two Decision regression models were performed: one with prior offenses and one without. The metrics for each model are listed below.  

  Model 1: 

    Features: Crime, Race, Gender, Prior offenses, Age, Pretrials attended, Court ORI 
    MSE: 0.06643128075622728        
    R2: 0.20073253482500297 

   Model 2: 

    Features: Crime, Race, Gender, Court ORI 
    MSE: 0.04463458242755976       
    R2: 0.4567274548877708 

3. K Nearest Neighbours Regression: 

Two KNN regression models were performed: one with prior offenses and one without. The metrics for each model are listed below. 

  Model 1: 

    Features: Crime, Race, Gender, Prior offenses, Age, Pretrials attended, Court ORI 
    R2: 0.4574613478907559 
    MSE: 0.04509321233472595 

  Model 2: 

    Features: Crime, Race, Gender, Court ORI 
    R2: 0.4623347733133504 
    MSE: 0.044173892266211 

SVR Model: 

Two SVR models were performed: one with prior offenses and one without. The metrics for each model are listed below.  

  Model 1: 

    Features: Crime, Race, Gender, Prior offenses, Age, Pretrials attended, Court ORI 
    R2: 0.5403899320034418 
    MSE: 0.03820058590622487   

  Model 2: 

    Features: Crime, Race, Gender, Court ORI 
    R2: 0.5269402945572196 
    MSE: 0.03886598468063764 

## Conclusion:
From this dataset, I was able to create successful models for each of our two goals: predicting bail and bail amount. The predicting bail model and the predicting bail amount had an 80% accuracy. To improve these models, I would like to collect more data, continue to finetune parameters, and update the data used as more cases come in. To expand the project I would like to create prediction models for other state judiciaries and compare the bail data available to find trends between states. The purpose of these models is to use them to create an interface that people can interact with to predict bail based on given conditions: age, gender, race, arrest type, prior criminal arrests, etc. The intent of making this interface is to help people understand what to expect as their bail at an arraignment, and to better inform the population about bail setting. 



