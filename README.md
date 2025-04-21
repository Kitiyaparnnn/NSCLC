# 🫁 NSCLC: Multi-classification of subtypes using Gene expression from RNA-sequence 

42698 Special Topics: Clinical Translation

by: Kitiyaporn Takham, Jainam Modh (assistant)

## Dataset 

GEO accession: **GSE81089**

Title: "Next Generation Sequencing (RNAseq) of non-small cell lung cancer"

Last update: Sep 08 2021

Original design: Fresh frozen tumor tissue from 199 patients diagnosed with NSCLC and surgically treated 2006-2010 at the Uppsala University Hospital, Uppsala, Sweden and 19 paired normal lung tissues. Clinical data were retrieved from the regional lung cancer registry.
Several of the new CTAs are poorly characterized

**Dataset rows**
- sample_id
  
**Dataset columns**
- gene_name
- Histology diagnosis spring 2013 HB (diagnosis_code): 1=squamous cell cancer, 2=AC unspecified, 3=Large cell/ NOS

## Machine Learning Model

CatBoost Classifier with class weight evaluated by balanced accuracy and F1 scores using SHAP for model interpretation
