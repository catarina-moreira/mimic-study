# CORE::Patient

Patients table


Information that is consistent for the lifetime of a patient is stored in this table.

## Detailed Description 

```diff
- subject_id [create an anchor](#anchors-in-markdown)
```
subject_id is a unique identifier which specifies an individual patient. 
Any rows associated with a single subject_id pertain to the same individual. 
As subject_id is the primary key for the table, it is unique for each row.

```diff
- gender
```
gender is the genotypical sex of the patient.

