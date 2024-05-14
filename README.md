# Fill in the blank, MIMIC the procedure: Tracking patient record for medical data reconstruction 
Strategy map : patient scenario with seven reconstruction rules

<img width="1163" alt="MIE2024_acceptmail_fill in blank_feature" src="https://github.com/sujungleeml/fillintheblank/assets/56566861/49a3247b-2925-4c03-a1ed-56c16dfef216">

We aimed to extract adult patients who experienced extubation from the MIMIC-IV database. Intubation and extubation are procedures that can occur more than once during hospitalization and display characteristics of being paired. For these adult patients, we employed a strategy involving patient scenario works that checked the temporal order and logical links of intubation/extubation data, and seven reconstruction rules for handling missing values.

EMR records are created by healthcare providers, which can lead to missing data. In the clinical domain, data related to dates and times, such as when a change occurred, the duration of a particular state, and when a diagnosis was made, are crucial. Traditional statistical methods have been used mainly to handle missing numerical values, such as blood pressure or pulse rate. However, we aimed to minimize data loss due to missing temporal information and maximize the utilization of available data. To achieve this, logical thinking based on knowledge and understanding of the healthcare environment and processes is necessary. We sought to perform data reconstruction consistently by using this logical thinking and excluding rules with low validity.

In particular, when setting the rules, we considered and reviewed all possible scenarios. For example, we replaced the end time of an event with the discharge time or time of death, but we did not use the admission time. This is because there is insufficient evidence in the clinical setting to support the idea that admission or ICU entry is the starting point for events such as intubation. Therefore, we excluded such cases from our rules. By designing data reconstruction rules that take into account the clinical context, we aimed to build a more accurate and reliable dataset.
