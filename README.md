# Medication Error Report

### Dashboard Link : https://1drv.ms/x/c/429eb989df50f199/EYSipVLkQ2VDtGqlh2rRXTgBdBxoPl2Fd02Wf5F8qjbiCA?e=IQW6lU

## Problem Statement

A medication error report dashboard is a visual representation of data related to medication errors within a healthcare setting. It provides an overview of key metrics, trends, and insights related to medication errors, helping healthcare professionals and administrators monitor, analyze, and address issues. 

The dashboard include information such as the number and types of errors, contributing factors, affected patients, trends over time, and the effectiveness of implemented corrective measures. By offering a consolidated and visualized view of medication safety data, the dashboard facilitates informed decision-making and continuous improvement efforts to enhance patient safety.

### Steps followed 

- Step 1 : Load data into Excel Desktop, dataset is a csv file.
- Step 2 : Open excel power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in some of the columns there were errors & empty values adequate data cleaning was carried out.
- Step 5 : In the report view, under the view tab, theme was selected.
- Step 6 : Since the dose unit column was cleaned to ensure data validation. 
- Step 7 : Visual filters (Slicers) were added for easy visualization of drug administration error over the years(2020 - 2022) and months. 
- Step 8 : Various  Visual like pie chart, line charts, bar charts, Paretto chart was used to show the various insights below;

  (a) The 20% of drugs responsible for 80% of drug error

  (b) Drug Administration error over the years (2020-2022)
  
  (c) Count of occurrence of medication error within the week
  
  (d) Nurses_id with most medication error

  (e) Top 10 patient_id served wrong medication dose
  
  (f) Relation between medication error and time of day

- Step 9 : In the report view, under the insert tab, five text boxes were added to the canvas, to show the Total number of Patient, the number of patient who have experience medication error ,the total number of nurse, percentage of nurse who served wrong dose of drug, Nurse_id with most medication error and patient_id with the highest occurence of wrong medication dose.

- Step 10 : In the report view, under the insert tab, using shapes option from elements group a rectangle was inserted & similarly using image option company's logo was added to the report design area. 

- Step 11 : A Paretto chart was created to visualize the 20% of drugs responsible for 80% of drug error.
        
- Step 12 : New measure was created to 
    i. validate drug dosage prescribed and drug dose administered
    ii. A column called condition was created to determine drugs administered accurately and wrongly.
    

Following Excel expression was written for the same,
        
        dosage_validation = =[@[prescribed_dose]] - [@[dose_administered]]

        condition = =IF([@[dosage_validation]]=0,"correct","error")
        
A card visual was used to represent count of Patients.

![pt_page-0001](https://github.com/FaeyO/Patient-Medication-Error-Report/assets/118575325/6df84f82-3dc0-4a7d-9413-1aa17da2ac25)


 - Step 13 : A Paretto chart was used to represent the 20% of drugs responsible for 80% of drug error.
 
 ![paretto_chart_page-0001](https://github.com/FaeyO/Patient-Medication-Error-Report/assets/118575325/e36624d8-add0-4f70-a5e3-2e763c17943e)

 
 - Step 14 : New measure was created to calculate the nature of the drug error ie over dose or under dose.
 
 Following EXCEL expression was written for the same,
 
         dosage_condition = =IF([@[dosage_validation]] > 0, "over dose", IF([@[dosage_validation]] = 0, "accurate dose", IF([@[dosage_validation]] < 0, "under dose", "")))

 - Step 15 : The report was then linked to Powerpoint and presented using Powerpoint.
 
# Insights

A single page report was created on Excel Desktop, and the following inferences can be drawn from the dashboard;

### [1] Total Number of Patients = 100

   Number of Patient who have experience medication error = 58(58%)

### [2] Total Number of Nurse = 15

   Number of Nurse who have served patient with wrong medication dose = 12 (80%)


### [3] Nurse id with most medication error     N1098


### [4] Patient id with most medication error  P075 
  
### [5] Some other insights
 
 ### The 20% of drugs responsible for 80% of drug error
    a)Penicillin
    b)levofloxacin
    c)Metronidazole
    d)Cefixime
    e)Ciprofloxacin
    
 ### Most medication error occurs :
    a)Wednesday
    b)Tuesday
    c)Sunday

![med_page-0001](https://github.com/FaeyO/Patient-Medication-Error-Report/assets/118575325/68d9b90b-151a-42bc-87a0-3500b7d7dee9)


### Dashboard view

![dailycensus_2259_pdf_page-0001](https://github.com/FaeyO/Patient-Medication-Error-Report/assets/118575325/e4cbdfa3-0e9d-4003-a3b8-4f09e8f10a72)

