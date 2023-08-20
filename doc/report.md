# Predicting Bail Status and Bail Amount

Presentation Link:
---link---

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

![image](https://github.com/vasavi0417/Veerla_Data606/assets/42056699/de6940d8-bca3-42a4-b9fc-566dc836a2e5)








