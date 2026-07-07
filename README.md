# Quality Improvement during neonatal transport

Jupyter Notebooks used for processing and analysis of clinical and ventilator parameters.


This repository contains the Python code used for data processing, statistical analysis and visualization described in the following paper:

**Lantos L, Szell A, Szanto G, Somogyvari Z, Belteki G. Safely developing respiratory care during emergency neonatal transport through systematic collection and analysis of detailed ventilator data. Eur J Pediatr. 2026 Jul 2;185(7):549. doi: 10.1007/s00431-026-07220-x. PMID: 42390585.**


Contact: gbelteki@aol.com; gusztav.belteki@nhs.net 

____

This code can be viewed in any web browser. If the code is displayed (rendered) in Github, copy and paste the URL (web adress) of the Notebook into [nbviewer](https://nbviewer.jupyter.org) for a read-only display.

To run the code, you can use Jupyter installed locally on your computer or [Google Colab](https://colab.research.google.com).

Raw data are not shared but users can run the code on their own data obtained in the same format.

____

Packages required to run this Notebook: numpy, pandas, matplotlib, scipy. For versions of Python and the add-on packages see the Notebooks. 

I recommend downloading these packages using Anaconda: [https://anaconda.org]([https://anaconda.org])

____

# Jupyter Notebooks


### A. Initial processing of raw ventilator slow (0.5 Hz) data

These notebooks perform the initial processing of ventilator data (including ventilator parameters, settings, alarms (0.5Hz sampling rate). Dictionaries containing the processed ventilator data exported as pickle archives: **data_pars_xxx_xxx.pickle** 

I. Data downloaded from the **fabian +nCPAP ventilator**:       cases AL000001 - AL001100
1. [ventilator_data_1_150](ventilator_data_1_150.ipynb):              AT000001 - AT000150
2. [ventilator_data_151_300](ventilator_data_151_300.ipynb):          AL000151 - AL000300
3. [ventilator_data_301_450](ventilator_data_301_450.ipynb):          AL000301 - AL000450
4. [ventilator_data_451_600](ventilator_data_451_600.ipynb):          AL000451 - AL000600
5. [ventilator_data_601_750](ventilator_data_601_750.ipynb):          AL000601 - AL000750
6. [ventilator_data_751_900](ventilator_data_751_900.ipynb):          AL000751 - AL000900
7. [ventilator_data_901_1050](ventilator_data_901_1050.ipynb):        AL000901 - AL001050
8. [ventilator_data_1051_1100](ventilator_data_1051_1100.ipynb):      AL001051 - AL001100

II. Data downloaded from the **fabian +HFOi ventilator**:           cases AT000001 - AT000818
1. [ventilator_data_new_1_150](ventilator_data_new_1_150.ipynb):          AT000001 - AT000150
2. [ventilator_data_new_151_300](ventilator_data_new_151_300.ipynb):      AT000151 - AT000300
3. [ventilator_data_new_301_450](ventilator_data_new_301_450.ipynb):      AT000301 - AT000450
4. [ventilator_data_new_451_600](ventilator_data_new_451_600.ipynb):      AT000451 - AT000600
5. [ventilator_data_new_601_750](ventilator_data_new_601_750.ipynb):      AT000601 - AT000750
6. [ventilator_data_new_751_900](ventilator_data_new_751_900.ipynb):      AT000751 - AT000900 
7. [ventilator_data_new_901_1050](ventilator_data_new_901_1050.ipynb):    AT000901 - AT001050
8. [ventilator_data_new_1051_1200](ventilator_data_new_1051_1200.ipynb):  AT001051 - AT001200
9. [ventilator_data_new_1201_1350](ventilator_data_new_1201_1350.ipynb):  AT001201 - AT001350
10. [ventilator_data_new_1351_1500](ventilator_data_new_1351_1500.ipynb): AT001351 - AT001500
11. [ventilator_data_new_1501_1650](ventilator_data_new_1501_1650.ipynb): AT001501 - AT001650
12. [ventilator_data_new_1651_1800](ventilator_data_new_1651_1800.ipynb): AT001651 - AT001800
13. [ventilator_data_new_1801_1950](ventilator_data_new_1801_1950.ipynb): AT001801 - AT001950

### B. Processing clinical data

I. [clinical_data_1_1100](clinical_data_1_1100.ipynb): Processing of clinical data related to recordings AL000001 - AL001100. DataFrame containing the processed clinical data exported as **clin_df.pickle** 

II. [clinical_data_new](clinical_data_new.ipynb): Processing of clinical data related to recordings AT000001 - AT001950. (Only cases up to AT001942 were included in this study). DataFrame containing the processed clinical data exported as **clin_df_new.pickle** 


### C. Processing of blood gases

I. [blood gases_1_1100](blood_gases_1_1100.ipynb): Processing of clinical data related to recordings AL000001 - AL001100. 

II. [blood gases_new](blood_gases_new.ipynb): Processing of clinical data related to recordings AT000001 - AT001950. (Only cases up to AT001942 were included in the study). 


### D. Further processing of slow (0.5Hz) ventilator data

I. [ventilator_data_processing_1_1100](ventilator_data_processing_1_1100.ipynb): Further processing of the 0.5 Hz ventilator data (measurements, settings and alarms) for recordings AL000001 - AL001100.

II. [ventilator_data_processing_new](ventilator_data_processing_new.ipynb):  Further processing of the 0.5 Hz ventilator data (measurements, settings and alarms) for recordings AT000001 - AT001950. (Only recordings up to AT001942 were included in this study).

 
### E. Manual trimming of the recordings

In these Notebooks, recordings have been individually inspected and trimmed to remove periods when the ventilator was working but the patient was not connected.

I. [ventilator_data_processing_1_1100_ventilated](ventilator_data_processing_1_1100_ventilated.ipynb): trimming of recordings AL000001 - AL001100. Recordings and recording parts with invasive mechanical ventilation are also identified.

IIa. [ventilator_data_trimming_new](ventilator_data_trimming_new.ipynb): trimming of recordings AT000001 - AT001950. (Only recordings up to AT001942 were included in this study).

IIb. [analysis_ventilated_new](analysis_ventilated_new.ipynb): Recordings and recording parts with invasive mechanical ventilation are  identified.

### F. Data analysis

Consider recordings `AL000001 - AL001100` and `AT000001 - AT001942` (up to 23/08/2025).

I. [Quality_improvement](Quality_improvement.ipynb): Processing and analysis of the impact of the a systematic quality improvement program on ventilation practice of the neonatal transport service. This work has been published [here](https://link.springer.com/article/10.1007/s00431-026-07220-x)

Study period: Every year between `2017 - 2025` (Ventilator data recording started in April 2017). Infants receiving conventional mechanical ventilation.

**Quality indicators:**

- QI-1. Proportion of conventional ventilation recordings where VG mode is used for >50% of the recording duration
- QI-1A. As Q1 but for a subgroup of infants born at <32 weeks gestation <14 days of age
- QI-2. Proportion of recordings with the conventional VG set between 4 - 6 mL/kg for ≥90% of the recording duration in infants <=14 days of age.
- QI-3. Mean expired tidal volume in the non-volume guaranteed recordings is between 4-6 mL/kg
- QI-4. Proportion of infants with a median difference between Pmax and PIP is is >=5 cmH2O in the VG recordings
- QI-5. At arrival pCO2  was >30 mmHg (4kPa) and either pCO2 was <52.5 mmHg (7 kPa) or pH was >7.2
- QI-6. Proportion of time spent with active ventilator alarms

