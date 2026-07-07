# Transport of extremely low birth infants on the first day of life

Jupyter Notebooks used for processing and analysis of clinical and ventilator parameters.


This repository contains the Python code used for data processing, statistical analysis and visualization described in the following paper:

**Stabilization, respiratory care and survival of extremely low birth weight infants transferred on the first day of life. Journal of Perinatology, in press**


Contact: gbelteki@aol.com; gusztav.belteki@nhs.net 

____


The outputs (numbers, tables, graphs) of the cells of the Jupyter Notebooks (.ipynb files) have been suppressed in order to comply with copyrights.
Some of the corresponding data and graphs can be found in the paper and its supplementary material.

This code can be viewed in any web browser. If the code is displayed (rendered) in Github, copy and paste the URL (web adress) of the Notebook into [nbviewer](https://nbviewer.jupyter.org) for a read-only display.

To run the code, you can use Jupyter installed locally on your computer or [Google Colab](https://colab.research.google.com).

Raw data are not shared but users can run the code on their own data obtained in the same format.

____

Packages required to run this Notebook: numpy, pandas, matplotlib, scipy. For versions of Python and the add-on packages see the Notebooks. 

I recommend downloading these packages using the freely availably Anaconda built: [https://anaconda.org](https://anaconda.org)

____

# Jupyter Notebooks


### A. Initial processing of raw ventilator slow (0.5 Hz) data

These notebooks perform the initial processing of ventilator data (including ventilator parameters, settings, alarms (0.5Hz sampling rate). Dictionaries containing the processed ventilator data exported as pickle archives: **data_pars_xxx_xxx.pickle** 

I. Data downloaded from the **fabian +nCPAP ventilator**: cases AL000001 - AL001100
1. [ventilator_data_1_150](ventilator_data_1_150.ipynb): cases AL000001 - AL000150
2. [ventilator_data_151_300](ventilator_data_151_300.ipynb): AL000151 - AL000300
3. [ventilator_data_301_450](ventilator_data_301_450.ipynb): AL000301 - AL000450
4. [ventilator_data_451_600](ventilator_data_451_600.ipynb): AL000451 - AL000600
5. [ventilator_data_601_750](ventilator_data_601_750.ipynb): AL000601 - AL000750
6. [ventilator_data_751_900](ventilator_data_751_900.ipynb): AL000751 - AL000900
7. [ventilator_data_901_1050](ventilator_data_901_1050.ipynb): AL000901 - AL001050
8. [ventilator_data_1051_1100](ventilator_data_1051_1100.ipynb): AL001051 - AL001100

II. Data downloaded from the **fabian +HFOi ventilator**: cases AT000001 - AT000818
1. [ventilator_data_new_1_150](ventilator_data_new_1_150.ipynb): AT000001 - AT000150
2. [ventilator_data_new_151_300](ventilator_data_new_151_300.ipynb): AT000151 - AT000300
3. [ventilator_data_new_301_450](ventilator_data_new_301_450.ipynb): AT000301 - AT000450
4. [ventilator_data_new_451_600](ventilator_data_new_451_600.ipynb): AT000451 - AT000600
5. [ventilator_data_new_601_750](ventilator_data_new_601_750.ipynb): AT000601 - AT000750
6. [ventilator_data_new_751_900](ventilator_data_new_751_900.ipynb): AT000751 - AT000900 (Only recordings up to AT000818 were included in this study)


### B. Processing clinical data

I. [clinical_data_1_1100](clinical_data_1_1100.ipynb): Processing of clinical data related to recordings AL000001 - AL001100. DataFrame containing the processed clinical data exported as **clin_df.pickle** 

II. [clinical_data_new_1_1397](clinical_data_new_1_1397.ipynb): Processing of clinical data related to recordings AT000001 - AT001397. (Only cases up to AT000818 were included in this study). DataFrame containing the processed clinical data exported as **clin_df_new.pickle** 


### C. Processing of blood gases

I. [blood gases_1_1100](blood_gases_1_1100.ipynb): Processing of clinical data related to recordings AL000001 - AL001100. Dictionary containing the processed blood gas data exported as pickle archive: **blood_gases_1_1100.pickle**

II. [blood gases_new_1_1397](blood_gases_new_1_1397.ipynb): Processing of clinical data related to recordings AT000001 - AT001397. (Only cases up to AT000818 were included in the study). Dictionary containing the processed blood gas data exported as pickle archive: **blood_gases_new.pickle**


### D. Further processing of slow (0.5Hz) ventilator data

I. [ventilator_data_processing_1_1100](ventilator_data_processing_1_1100.ipynb): Further processing of the 0.5 Hz ventilator data (measurements, settings and alarms) for recordings AL000001 - AL001100.

Imported: **data_pars_xxx_xxx.pickle**, **clin_df.pickle**

Exported: dictionaries containing ventilation data as **data_pars_measurements_1_1100.pickle,  data_pars_settings_1_1100.pickle, data_pars_alarms_1_1100.pickle**

II. [ventilator_data_processing_new_1_1305](ventilator_data_processing_new_1_1305.ipynb):  Further processing of the 0.5 Hz ventilator data (measurements, settings and alarms) for recordings AT000001 - AL001305. (Only recordings up to AT000818 were included in this study) 

Imported: **data_pars_new_xxx_xxx.pickle**, **clin_df_new.pickle**

Exported: dictionaries containing ventilation data as **data_pars_measurements_new_1_1305.pickle,  data_pars_settings_new_1_1305.pickle, data_pars_alarms_new_1_1305.pickle**
  
 
### E. Manual trimming of the recordings

I. [ventilator_data_processing_1_1100_ventilated](ventilator_data_processing_1_1100_ventilated.ipynb): This notebook ventilator data to keep only periods of mechanical ventilation. Recordings have also been individually inspected and trimmed to remove periods when the ventilator was working but the patient was not connected.

Imported: **data_pars_measurements_1_1100.pickle,  data_pars_settings_1_1100.pickle, data_pars_alarms_1_1100.pickle**, **clin_df_1_1100.pickle**

Exported: **data_pars_measurements_ventilated_1_1100.pickle, data_pars_settings_ventilated_1_1100.pickle, data_pars_alarms_ventilated_1_1100.pickle, vent_modes_ventilated_1_1100.pickle**


II. [ventilator_data_trimming_new_1_1305](ventilator_data_trimming_new_1_1305.ipynb): In this Notebook, recordings have been individually inspected and trimmed to remove periods when the ventilator was working but the patient was not connected. (Only recordings up to AT000818 were included in this study) 

Imported: **data_pars_measurements_new_1_1305.pickle,  data_pars_settings_new_1_1305.pickle, data_pars_alarms_new_1_1305.pickle**, **clin_df_new.pickle**

Exported: **data_pars_measurements_trimmed_new_1_1305.pickle,  data_pars_settings_trimmed_new_1_1305.pickle, data_pars_alarms_trimmed_new_1_1305.pickle, 
vent_modes_trimmed_new_1_1305.pickle**


### F. Analysis of clinical and ventilator data of ELBW (<1000 g birth wieight) infants transferred during the first 24 hours of their life.

Consider recordings `AL000001 - AL001100` and `AT000001 - AT000818`.

These Notesbooks use the pickle archives exported by the above Notebooks.

1. [ELBW_analysis_ventilation](ELBW_analysis_ventilation.ipynb): Analysis of ventilator data of ELBW infants (born with <1000 g birth weight) who were transferred ventilated ex utero in the first 24 hours of life.

2. [ELBW_analysis_clinical](ELBW_analysis_clinical.ipynb): Analysis of manually collected clinical data for the above group, in relation to to the respiratory care of the patients.
