#  Dataset-Epidemiologic-Investigation-COVID19

## Introduction

This repository contains a dataset of entity, relation and event recognition on
epidemiological case reports.
If you use this dataset, please cite our paper: 

```Jian Wang, Ke Wang, Jing Li, Jianmin Jiang, Yanfei Wang, Jing Mei
Accelerating Epidemiological Investigation Analysis by Using NLP and
Knowledge Reasoning: A Case Study on COVID-19
AMIA 2020, submission```


We collected the epidemiological case reports from Dec 19, 2019
to Feb 7, 2020 from the websites of China CDC and some main-stream news websites. This repository 
was created from the case reports which were labelled by manual with entities, relations, 
and events. 

Special thanks to China CDC and the subbranchs in local cities. Lots of the data are from their announcements.
We also appreciate the following news websites some of the data are from: sina.com.cn, people.com.cn, thepaper.cn and news.163.com 
etc. 

## Data Format

All the data (train, validation, test) are in json format. For each line of the data, it's 
a case report with following json keys:

text: The original plain text of the case report
entities: All labelled entities in the text. The elements of the entity is start offset in 
text, end offset and the entity type. Entity types include: 

- 'LocalID' : the patient ID in a city
- 'Name' : the family name of the patient if there is, 
- 'Age' : the age of the patient
- 'Gender' : the gender of the patient
- 'ResidencePlace' : the residence place of the patient
- 'SuspectedPatientContact' : if current patient has or has not the history of contacting suspected COVID-19 patient
- 'InfectionOriginContact' : if current patient has or has not the history of trip to the COVID-19 origin regions or contacting the passager(s) from COVID-19 origin regions
- 'Event' : a verb to indicate an activity in activity records
- 'Onset' : a verb to indicate the event of disease onset
- 'HospitalVisit' : a verb to indicate the event of seeing a doctor
- 'DiagnosisConfirmed' ：a verb to indicate the event of being confirmed as COVID-19 disease
- 'Inpatient' : a verb to indicate the event of admission as a COVID-19 patient
- 'Discharge' : a verb to indicate the event of discharging
- 'Death' : a verb to indicate the event of death
- 'Observed' : a verb to indicate the event of being observed as a suspected COVID-19 patient
- 'Date' : the date or time . or the start date/time for a duration
- 'EndDate' : the end date/time for a duration
- 'Symptom' : Symptom words
- 'LabTest' : Lab test
- 'ImagingExamination' : Imaging examination
- 'Location' : City or privince
- 'Spot' : a spot, such as hotel, building, station, home, etc.
- 'Vehicle' : a vehicle, such as train, bus, car, ship, airplan and so on.
- 'SocialRelation' : Social relations, such as relatives relation, classmate, colleague and so on.
- 'Negation' : negation words

