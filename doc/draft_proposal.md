# DATA 606: Capstone Project
## **Title:** Predicting the bail status and bail amount

- **Author:** Snigdha Panakanti
- **Term:** Summer 2023

**Introduction:**

People do not often think about arraignment cases and how bail is set in their day-to-day lives. However, they become important when people or people they know are involved in these processes. During an arraignment, both the prosecution and the defence say what they think about bail and give important information about the arrest and the defendant's criminal past. The judge then chooses if the bail should be set, how much bail should be, and any other rules that do not involve money. There are questions about how fair bail is because the judge's choice can be affected by many things. Even though the crime itself might seem to be the most important reason, other things like gender, race, and even the judge's own life could play a role. 

In the 2019 book "Talking to Strangers" by Malcolm Gladwell, he looks at how well judges set bail. Gladwell talks about a study by economist Sendhil Mullainathan and a group of computer scientists. They used data from New York City from 2008 to 2013 to make an AI machine. This machine made a list of people who could be released from jail to wait for their trial at home. When the AI machine's predictions were compared to what the judges did, it was found that the people on the machine's list were 25% less likely to commit a crime while waiting for trial. The study also showed that judges set bail for people based on where they fell on an AI machine's risk scale. This randomness in bail choices makes me wonder if people or machines are better at making bail decisions.

This study aims to look at the New York State Pre-Trial data, which is a large set of information about charges and court appearances in New York. The focus will be on how gender, race, and the choice to set bail and the amount of bail are related. Based on this information, models will be made to predict whether bail will be set and how much it will be. The end goal is to let suspects and their families put their information into these models before the arraignment so they can get an idea of what the bail might be. This study hopes to make setting bail more fair and clear by looking at these factors and using predictive modeling.

**Background and Significance:**

Machine learning techniques have been looked at in the past as a way to improve the bail process. The way things are now, there is no oversight, so judges have to use their own opinion to decide how much bail to set. This is a very hard job because each case has its unique details. This makes it hard for judges to weigh the possible benefits and risks properly. Studies have also shown that environmental factors, such as being tired of making decisions, can greatly affect how the justice system works. For example, judges may have different rates of granting release at the beginning and end of the day because they are mentally tired and can make decisions more quickly.

To deal with these worries, some places, like New Jersey, have implemented algorithmic risk assessment models that rate how dangerous each suspect is. Proponents of these models say they can help reduce bias in bail choices and lessen the need for cash bail, affecting people from lower socioeconomic backgrounds more than others. Critics point out, though, that the data used to make these algorithms may reflect racial and socioeconomic differences in crime and police that are already there.

The goal of moving toward risk assessments is to find a balance between public safety, the efficiency of the justice system, and the well-being of people and groups. However, the benefits of putting these assessments into place have been mixed. Even though there have been some good results, like more defendants being released on their recognizance, there have also been problems with how bail choices are made, especially regarding minority defendants.

Given how hard it is to decide bail, this project aims to model bail decisions using machine learning. This study aims to find out what factors affect bail decisions by making a model that predicts the outcomes of current court decisions. This project is important because it could help people understand how the bail process works and add to the current conversations about fairness, transparency, and equity in the criminal justice system. By looking at the New York State Pre-Trial data, this study hopes to learn more about how gender, race, and other factors affect bail choices.

**Objective:**

Two different parts of the information will be looked at in this project. The first goal is to look at the records to see if bail has been set. The second goal of the project is to make models that can predict if bail will be set and how much it will be. The goal of the prediction models is to create a way for people to put their information (age, gender, charge, severity of charge, previous crimes, etc.) and find out what their bail will be.

**Data Source and Quality:**

The dataset used for this project is retrieved from the official website of the New York State Unified Court System at https://ww2.nycourts.gov/pretrial-release-data-33136. The source is highly credible as it is provided directly by the court system. The dataset is of high quality, containing comprehensive information related to pretrial release decisions in New York. The size of the dataset and specific attributes will be further explored during the data analysis phase.

**Unit of Analysis and Dataset Size:**

The unit of analysis in this project is individual cases within the criminal justice system. Each case represents a unique observation, capturing information such as defendant characteristics, offense details, pretrial release decisions, and case outcomes. The dataset contains a substantial number of observations, allowing for robust analysis and modeling.
The dataset is a .csv file that is 194MB in size and has 108 columns and 284096 rows.

**Variables/Measures:**

This data set contains information from about 63 courts in and around New York City. Different courts can make different choices about arraignment release, and the exact details were also written down in the data. We have separated the data into groups to test different theories based on our information. Gender, Race, Ethnicity, Age at crime and arrest, Arraign Charge Category, Representation Type in court, Release Decision at Arraign, Bail Amount, and Arrest Type are the most used columns in the dataset for all theories. 

The variables/measures planned for analysis include:

- Defendant demographics (age, gender, race, etc.)
- Offense characteristics (type of offense, severity, etc.)
- Pretrial release decisions (bail amount, release type, conditions, etc.)
- Case outcomes (dismissal, conviction, etc.)
- Recidivism rates

These variables are essential for understanding the factors influencing pretrial release decisions and evaluating their impact on case outcomes and recidivism rates.

**Techniques/Models:**

The project will employ various techniques and models, including but not limited to:

Descriptive statistics and data visualization to explore patterns and distributions.
Logistic regression to analyze the factors influencing pretrial release decisions.
Machine learning algorithms such as decision trees, random forests, or support vector machines to develop predictive models for pretrial release decisions and recidivism rates.

**Model Evaluation and Comparison:**

The performance of the models will be evaluated using appropriate evaluation metrics, such as accuracy, precision, recall, and F1-score. Cross-validation techniques will be employed to assess the models' robustness and generalizability. The models will be compared based on their predictive accuracy, fairness, and ability to mitigate biases in pretrial release decisions.

**Intended Outcomes:**

The project aims to achieve the following outcomes:

Gain a better understanding of the factors influencing pretrial release decisions.
Identify potential biases or disparities in the pretrial release process.
Develop predictive models to assist in fair and accurate pretrial release decisions.
Provide insights and recommendations to policymakers and criminal justice stakeholders for improving the pretrial release process.

**Deployment of Trained Model:**

The trained model can be deployed through a web application or dashboard using frameworks such as Streamlit, Dash, or Flask. This would enable users, such as judges, lawyers, or policymakers, to input relevant case information and receive predictions or recommendations for pretrial release decisions. The deployment would enhance decision-making processes and promote transparency and fairness in the pretrial release system.

**Conclusion:**

In conclusion, the Bail Bond Project aims to address the issue of pretrial release and its impact on the criminal justice system. By analyzing factors that influence pretrial release decisions, evaluating biases and disparities, and examining the impact on recidivism rates, this project strives to promote fairness, transparency, and efficiency in the pretrial release process. Through the use of descriptive statistics, logistic regression, and machine learning models, the project intends to provide valuable insights and recommendations to policymakers and stakeholders. The ultimate goal is to foster a better understanding of the issue, develop tools for informed decision-making, and contribute to the creation of a more equitable and effective criminal justice system.

**References:**

- Division of Technology & Court Research. (2022). Pretrail Release Data [CSV]. Retrieved from
https://ww2.nycourts.gov/pretrial-release-data-33136

- Gladwell, M. (2019). Getting to Know der Fuhrer. In Talking to Strangers (pp. 36–43).
essay, Little, Brown, and Company.
