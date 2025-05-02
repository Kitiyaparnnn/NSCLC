# 🫁 NSCLC: Multi-classification of subtypes using Gene expression from RNA-sequence 

42698 Special Topics: Clinical Translation

by: Kitiyaporn Takham, Jainam Modh (assistant)

## Dataset 

GEO accession: [**GSE81089**](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE81089)

Title: "Next Generation Sequencing (RNAseq) of non-small cell lung cancer"

Last update: Sep 08 2021

Original design: Fresh frozen tumor tissue from 199 patients diagnosed with NSCLC and surgically treated 2006-2010 at the Uppsala University Hospital, Uppsala, Sweden and 19 paired normal lung tissues. Clinical data were retrieved from the regional lung cancer registry.
Several of the new CTAs are poorly characterized

**Dataset rows**
- sample_id (199 people)
  
**Dataset columns**
- gene_name (64,253 genes)
- Histology diagnosis spring 2013 HB (diagnosis_code): 1=squamous cell cancer, 2=AC unspecified, 3=Large cell/ NOS

## Machine Learning Model

CatBoostClassifier(gradient boosting + decision tree) integrated with weighted configuration (using class weight) and PCA as a dimensional reduction.  The model is evaluated by using balanced accuracy and F1 scores. SHAP is used to interpret the model.

**Training pipeline:**
- 5-fold cross-validation
- 25 PCA components
- bootstrap_type: Bayesian
- depth: 3
- iterations: 300
- l2_leaf_reg: 5
- learning_rate: 0.05

**Performance**
- Train Accuracy: 94.89%
- Test Accuracy: 69.39%
- F-1 score: 
  - Squamous cell (0.812)
  - AC unspecified (0.789)
  - Large cell (0.400)


