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

