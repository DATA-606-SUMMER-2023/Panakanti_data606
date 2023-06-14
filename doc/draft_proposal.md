# Project Proposal

## Title: Predicting Bail Decisions and Bail amounts
- **Author:** Snigdha Panakanti
- **Term:** Summer 2023

### Abstract
The goal of this project plan is to find ways to detect fake news using Python and machine learning. The spread of fake news in the digital age has big effects on society, so it's important to find ways to spot and stop it. This proposal explains why this problem is important, what questions need to be answered, where the data comes from, what the variables are, how the data will be analyzed, how the model will be evaluated, what the expected results are, and how the trained model will be used.

### Introduction
The Bail Bond Project aims to analyze and explore the issue of pretrial release and its impact on the criminal justice system. This proposal outlines the motivation behind the project, the questions to be answered, the dataset to be used, the unit of analysis, variables/measures, techniques/models, evaluation methods, and intended outcomes.

- #### Issue of interest and its importance
The Bail Bond Project is interested in the topic of pretrial release and how it affects the criminal justice system. Pretrial release is the practice of releasing suspects from detention prior to their trial date under particular circumstances, such as the posting of bail or compliance with rules. The fairness and efficiency of the criminal justice system are directly impacted by this issue, making it of paramount importance.

Pretrial release is the practice of releasing suspects from custody before their trial, providing they meet specific requirements. Because it directly impacts the fairness and efficiency of the criminal justice system, the issue of pretrial release is very important. In order to uphold the maxim "innocent until proven guilty" and cut down on needless pretrial detention, it is essential to provide a fair and effective pretrial release process.

Potential biases and inequities within the system can be revealed by understanding the elements that affect choices about pretrial release, such as demographic traits, the seriousness of the offense, and prior criminal history. By addressing these problems, the project seeks to advance fairness, openness, and well-informed judgment in the pretrial release procedure.

The Bail Bond Project aims to increase fairness, openness, and efficiency in the pretrial release process by examining these issues, contributing to our understanding of pretrial release practices, identifying potential biases, and offering policy and decision-makers insights.

### Research Questions
The project aims to answer the following research questions:

- Can the Bail decisions be predicted?
- Can the Bail amount be estimated?

### Data Sources
The dataset used for this project is retrieved from the official website of the New York State Unified Court System at https://ww2.nycourts.gov/pretrial-release-data-33136. The source is highly credible as it is provided directly by the court system. The dataset is of high quality, containing comprehensive information related to pretrial release decisions in New York. The size of the dataset and specific attributes will be further explored during the data analysis phase.
 
####  Unit of Analysis and Dataset Size
The unit of analysis in this project is individual cases within the criminal justice system. Each case represents a unique observation, capturing information such as defendant characteristics, offense details, pretrial release decisions, and case outcomes. The dataset contains a substantial number of observations, allowing for robust analysis and modeling.

- This dataset has a shape of **284098 X 108**.
- The memory usage for this dataset takes up **234.1+ MB** of space.

- #### Variables/Measures
The variables/measures planned for analysis include:

- Defendant demographics (age, gender, race, etc.)
- Offense characteristics (type of offense, severity, etc.)
- Pretrial release decisions (bail amount, release type, conditions, etc.)
- Case outcomes (dismissal, conviction, etc.)
- Recidivism rates
These variables are essential for understanding the factors influencing pretrial release decisions and evaluating their impact on case outcomes and recidivism rates.

### Techniques/Models
The project will employ various techniques and models, including but not limited to:

Descriptive statistics and data visualization to explore patterns and distributions.
Logistic regression to analyze the factors influencing pretrial release decisions.
Machine learning algorithms such as decision trees, random forests, or support vector machines to develop predictive models for pretrial release decisions and recidivism rates

### Model Evaluation and Comparision
The performance of the models will be evaluated using appropriate evaluation metrics, such as accuracy, precision, recall, and F1-score. Cross-validation techniques will be employed to assess the models' robustness and generalizability. The models will be compared based on their predictive accuracy, fairness, and ability to mitigate biases in pretrial release decisions.

### Intended Outcomes
The intended outcomes of this project include:

- Improve your knowledge of the elements affecting decisions regarding pretrial release.
- Determine any possible biases or inequities in the pretrial release procedure.
- Create prediction algorithms to help with just and accurate pretrial release judgments.
- Offer policymakers and criminal justice stakeholders perspectives and suggestions for enhancing the pretrial release procedure.

### Model Deployment
Frameworks like Streamlit, Dash, or Flask can be used to deliver the trained model through a web application or dashboard. Users, such judges, attorneys, or policymakers, could enter pertinent case information and get forecasts or suggestions for decisions about pretrial release as a result. With the deployment, decision-making procedures would be improved, and the pretrial release system would be made more open and equitable.

### Conclusion
Let's sum up by saying that the goal of the Bail Bond Project is to address the problem of pretrial release and its effects on the criminal justice system. This study seeks to further fairness, openness, and efficiency in the pretrial release procedure by investigating the variables that affect choices about pretrial release, assessing biases and disparities, and looking at the effect on recidivism rates. The initiative seeks to give policymakers and stakeholders useful information and advice by utilizing descriptive statistics, logistic regression, and machine learning algorithms. The ultimate objective is to promote a greater comprehension of the problem, create resources for informed decision-making, and contribute to the development of a criminal justice system that is more equal and efficient.

### References
- [Kaggle: Detecting Fake News Step by Step](https://ww2.nycourts.gov/pretrial-release-data-33136)
