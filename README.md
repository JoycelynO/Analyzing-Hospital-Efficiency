# Analyzing-Hospital-Efficiency
This project analyses New York State-Wide Hospital discharge data for a year(2022) to measure hospital efficiency using Length of Stay(LOS) and Discharge Costs as KPIs. Elective Hip Replacement surgery was the main reason for their hospital stay. 

## Project Background
Due to the fragmented nature of the US Healthcare System, high costs and quality of healthcare providers is one area that has opportunities for improvement. According to the 
Kaiser Family Foundation, relative to the size of its economy, the US spends a disproportionate amount on healthcare. In 2009 it was estimated that $765 billion was wasted annually. Unnecessary services was 210 billion. Excess administrative care is estimated to be 190 billion, and the prices that are too high are about 105 billion.
This project provides insights that will help a health consulting team(Health Stat) identify areas for improvements in hospital efficiency, one of the six dimensions in healthcare quality. Hospital Managements seek to reduce Length of Stays and costs while not compromising the quality of patient care.

Insights and Recommendations are provided on the following key areas:
1. Which hospitals have the highest average cost and LOS relative to the state averages?
2. Which hospitals stand out as outliers overall?
3. What factors influence LOS and Cost the most?

Interactive Power BI Report: 

## Data Structure
The focus of this analysis is patients who received hip replacement surgeries in the New York State, a common and resource-intensive procedure. Patients with hip pain, normally athritis require a hip replacment procedure. Hospital stays typically last from 0 to 2days or more. Data is sourced from the New York State SPARCS website. 
The dataset is one single table with 30 columns. Each row in the dataset represents a single inpatient stay, from their admission to discharge date.
The health information in this dataset is not individually identifiable for privacy reasons. 

Some key attributes of interest for the project are: a unique identifier for the hospital facility, a grouping of patient age, patient's disposition, the diagnosis description, severity of illness, and risk of mortality.

Key Terminology:
1. Inpatient: a person who has been admitted to a hospital bed.
2. Discharge: the release of a patient from hospital care by a medical worker.
3. Disposition: the patient destination or status upon discharge, for instance to another facility or to home.
4. Elective surgery: a procedure that was planned in advance, in other words, it was not due to an emergency.

## Data Preparation in Power BI
1. Built a calculated table to organize all calculated measures.
2. Calculated % Variance Average cost per discharge, % Variance average LOS Days for differences between overall state average and hospital average.
3. Calculated Average LOS, Average cost of discharge, Total hospitals, surgeons, then, created age bins.
4. Built a calculated table from the hospital discharges table to calculate a proxy for surgical program volume summary using the Summarize Columns function in DAX. Then built bins for surgical program size and total discharges.
5. Created a dynamic hospital profile title using the Values function in DAX.
6. DAX Measures used include: Calculate, Average, ALL, Summarize Columns, Values and Divide

## Insights and Recommendations
1. The New York City Service Area had the highest percentage of hospitals performing the surgical procedure of interest. The NYU Lutheran Medical Center, Olean General Hospital and Memorial Hospital for Cancer and Allied Diseases had the highest average cost per discharge (304.59%, 288.64% and 207.20% respectively) relative to the overall state average ($20,910).
   
2. The Kings County Hospital Center, Interfaith Medical Center and Memorial Hospital for Cancer and Allied Diseases had the highest LOS days(352.59%, 252.01%, 243.14% respectively relative to the overall state average(2.65days)
These hospitals stood out as outliers overall.

3. A root cause analysis revealed some key drivers stood out over others to influence both cost and average LOS:
- Patients who had an extreme illness severity and extreme major mortality risk stood out as having the most significant impact on reduced efficiency.
- Hospitals in New York City tended to have a higher cost and LOS overall. This could be due to the higher cost of living and operational expenses in the city.
- LOS was heavily influenced by patient disposition to a skilled nursing home.

Recommendations: 
- The consulting company should advise hospitals to:
  1. develop and implement risk stratification models to identify high-risk patients early in their care journey.
  3. build stronger partnerships with skilled nursing facilities to improve care coordination and reduce delays.
  4. conduct a detailed review of supply chain and operational processes for hospitals in the New York City service area to identify cost-saving opportunities.
  5. compare costs with hospitals performing below the state average to identify best practices.
- Targeted interventions should be made for outlier hospitals first, as they offer the greatest potential for improvement.
