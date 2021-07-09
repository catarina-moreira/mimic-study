# CORE::Admissions

Admissions table

The admissions table gives information regarding a patient’s admission to the hospital. Since each unique hospital visit for a patient is assigned a unique hadm_id, the admissions table can be considered as a definition table for hadm_id. Information available includes timing information for admission and discharge, demographic information, the source of the admission, and so on.

## Detailed Description 

The admissions table defines all hospitalizations in the database. Hospitalizations are assigned a unique random integer known as the hadm_id.


```diff
- subject_id, hadm_id
```
Each row of this table contains a unique hadm_id, which represents a single patient’s admission to the hospital. 
hadm_id ranges from 2000000 - 2999999. It is possible for this table to have duplicate subject_id, indicating that 
a single patient had multiple admissions to the hospital. The ADMISSIONS table can be linked to the PATIENTS table 
using subject_id.

```diff
- gender
```
gender is the genotypical sex of the patient.

```diff
- admittime, dischtime, deathtime
```
admittime provides the date and time the patient was admitted to the hospital, while dischtime provides the date and time the patient was discharged from the hospital. If applicable, deathtime provides the time of in-hospital death for the patient. Note that deathtime is only present if the patient died in-hospital, and is almost always the same as the patient’s dischtime. However, there can be some discrepancies due to typographical errors.

```diff
- admission_type
```
admission_type is useful for classifying the urgency of the admission. There are 9 possibilities: ‘AMBULATORY OBSERVATION’, ‘DIRECT EMER.’, ‘DIRECT OBSERVATION’, ‘ELECTIVE’, ‘EU OBSERVATION’, ‘EW EMER.’, ‘OBSERVATION ADMIT’, ‘SURGICAL SAME DAY ADMISSION’, ‘URGENT’.

```diff
- admission_location, discharge_location
```
admission_location provides information about the location of the patient prior to arriving at the hospital. Note that as the emergency room is technically a clinic, patients who are admitted via the emergency room usually have it as their admission location.

Similarly, discharge_location is the disposition of the patient after they are discharged from the hospital.

```diff
- insurance, language, marital_status, ethnicity
```
The insurance, language, marital_status, and ethnicity columns provide information about patient demographics for the given hospitalization. Note that as this data is documented for each hospital admission, they may change from stay to stay.

```diff
- edregtime, edouttime
```
The date and time at which the patient was registered and discharged from the emergency department.

```diff
- hospital_expire_flag
```
This is a binary flag which indicates whether the patient died within the given hospitalization. 1 indicates death in the hospital, and 0 indicates survival to hospital discharge.





