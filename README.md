## Luumurrud

Andmete failid (xlsx-id, csv-d):

- struktuuri, tunnuste kirjelduse
- kirjeldava skeemi luumurru, selle ravi ja ravifaaside kohta
- võimalikud uurimisküsimused

Pidime paari tunnust modifitseerima, et mitme tunnuse alusel poleks võimalik kellegi vanaisa või vanaema tuvastada.

Täpsemalt modifitseerisime järgmisi tunnuseid:

- vanus - lisasime randomiseeritult -2 ... -1 või +1 ... +2
- luumurru saamise kuupäev - lisasime randomiseeritult -91... -31 või + 31 ... 91 päeva (lisasime selle kõigile kuupäevadele, mistõttu patsientide elulemus, aeg operatsioonini jne jäid samaks).

Andmed: Pärt Prommik

================================

## Hip fracture data

Estonian hip fracture data from Jan 2009-Oct 2017 (modified)
Structure of the dataset and descriptions of the variables

### ABBREVIATIONS:
PAC – post-acute care
LOS – length of hospital stay (measured in days)
n/a – not available or missing value

### SUMMARY FILE (COLUMNS)
Patients' characteristics:

+	id -- anonymised patient's identification number
+	sex -- f - female; m - male
+	age -- in years
+	county -- county of residence
+	Comorbidities. 19 disease categories, all binary variables (1 – disease, 0 – no disease):
      - comorbidity -- Charlson comorbidity score
      - myocardial_infarction, 
      - congestive_heart_failure, 
      - peripheral_vascular_disease, 
      - cerebrovascular_disease, 
      - dementia, 
      - chronic_pulmonary_disease, 
      - rheumatic_disease, 
      - peptic_ulcer_disease, 
      - diabetes, 
      - hemi-paraplegia, 
      - renal_disease, 
      - any_malignancy, 
      - liver_disease, 
      - metastatic_solid_tumor, 
      - aids-hiv, 
      - alcohol_abuse, 
      - obesity, 
      - psychoses, 
      - depression
+	Fracture 
+ Time
+	date_of_fracture -- actually it is date of hospitalisation, but mostly they are the same
+ year -- year of fracture
+	Type
      -	fracture_type -- 3 values: femoral_neck, pertrochanteric, subtrochanteric
+	Acute care (1st step care). Fracture treatment some variable include missing values (N/A) for operated patients
    -	operation_date 
    -	days_to_operation – time from acute hospitalisation to operation in days
    -	operation_weekday – 1 – Monday, 2 Tuesday …
    -	management_method –values: conservative, hemiarthroplasty, total hip arthroplasty, osteosynthesis
+	Length of stay and physical therapy received
    -	acute_LOS – integer variable, acute length of stay in days
    -	acute_therapy – scale variable, physical therapy received during acute care
+	Post-acute care (2nd step care). Length of hospital stay
      -	post-acute_LOS – integer variable, total post-acute length of stay in days (includes all hospitalisations)
      -	post-acute_therapy – scale variable, total post-acute physical therapy received in hours (includes all in- and outpatient settings)
      -	PAC_type – post-acute care type: patients were subgrouped by received post-acute in- and outpatient care
+ Survival. Variables presented as time (time period, m – month [in days or in months]) and status (1 – event of death occurred; 0 – alive at that time point). 
      -	time_3m
      -	status_3m
      -	time_12m
      -	status_12m

### POST-ACUTE DATA ONLY (ROWS)
+	Patients' characteristics
    -	id -- anonymised patient's identification number
    -	invoice_number – post-acute invoices were numbered consecutively by date
    -	invoice_start – invoice start date
    -	invoice_end – invoice end date
    -	post-acute_type – type of setting (i simplified this part for the course, since defining these types would take much time)
    -	LOS – length of stay in days in this setting, zeros are for outpatient settings
    -	therapy – total physical therapy received in that setting

### BOTH TABLES JOINED
Check above.
