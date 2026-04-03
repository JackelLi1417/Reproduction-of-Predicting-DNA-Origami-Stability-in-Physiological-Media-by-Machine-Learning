This readme file was generated on [2026-4-2] by [Jianqiu Li, Yujie Song]

-------------------
GENERAL INFORMATION
-------------------

Title of Dataset:
Data from: Predicting DNA Origami Stability in Physiological Media by Machine Learning;
Data and scripts from: https://github.com/molML/DNA-origami-stability-prediction

Author Contact Information (Name, Institution, Email, ORCID)

	Principal Investigator(s): Francesca Grisoni
	Institution: Department of Biomedical Engineering, Institute for Complex Molecular Systems, Eindhoven University of Technology, Eindhoven, The Netherlands; Centre for Living Technologies, Alliance TU/e, WUR, UU, UMC Utrecht, Utrecht, The Netherlands
	Email: f.grisoni@tue.nl
	ORCID: 0000-0001-8552-6615

	Associate or Co-investigator: Tania Patino Padial
	Institution: Department of Biomedical Engineering, Institute for Complex Molecular Systems, Eindhoven University of Technology, Eindhoven, The Netherlands
	Email: t.patino.padial@tue.nl
	ORCID: 0000-0001-9979-7926

	Alternate Contact(s): N/A

Problem being solved:
Mapping 5 material features and 1 structual feature to diffusion coefficient.

Machine learning approach:
 Random forest regressor (denoted as RF), support vector regressor (denoted as SVR), Gaussian process regressor (denoted as GPR) and XGBoost.

--------------------
DATA & FILE OVERVIEW
--------------------

File list (filenames, directory structure (for zipped files) and brief description of all data files):
4 files in the code folder: 
workflow.ipynb file: does all the machine learning workflow.
df_rods.csv: contains all the predicted diffusion coefficients and metric for the rod structure out of the grid from datas.csv.
df_spheres.csv: contains all the predicted diffusion coefficients and metric for the sphere structure out of the grid from datas.csv.
df_rectangles.csv: contains all the predicted diffusion coefficients and metric for the rectangle structure out of the grid from datas.csv.
5 files in the me_dataset folder: 
datas.csv: contains the grid of parameter set we used to make prediction for the best diffusion coefficient we want; 
new_experiments_df.csv: contains 81 data points at the boundary or out of the range from new experiments 
raw_data_origami_FULL.csv: all 1417 original data samples;
raw_data_origami_HELDOUT.csv: 1317 training data samples;
raw_data_origami_TRAIN.csv: 100 data samples from farthest sampling methods;

--------------------------
METHODOLOGICAL INFORMATION
--------------------------

Description of methods used for collection/generation of data: 

Running on Python notebook.

--------------------------
DATA-SPECIFIC INFORMATION 
--------------------------

Variable/field list
Define each including spelling out abbreviations
We have six variables: the structure of the origami, the temperature, the concerntration of the magnesium chloride, the incubate time, the pH value, the DNase I concentration.
For the origami structure, we have three different structures: icosahedrons, rectangles, rods. For the temperature, it's the solution temperature. For the magnesium chloride concerntration, it's the final concerntration of the magnesium chloride. For the incubate time, it includes all the processes of annealing that occur in the PCR instrument. For the pH value, it's the solution pH value. For the DNase I concentration, the DNase I is an enzyme that cuts DNA. Its main function is to break down the DNA strands, that is, to degrade the complete DNA into shorter fragments. Also the concentration means the final concentration of the DNase I.
 
Value/attribute list
Include units of measure, codes or symbols used
For the origami structure, they were pre-designed with a specific structure. For the temperature, we get this value from the PCR facility and the unit is degree centigrade. For the magnesium chloride concerntration, the unit is millimol per liter. For the incubate time, the unit is hour. For the pH value, there is no unit. For the DNase I concentration, the unit is unit per milliliter. The unit here means the enzyme activity unit, we can get the data from the Reagent Instruction Manual.
   
We use the train_test_split function from sklearn.model_selection to randomly split data sets for training and validation. 

-------------------------
USE and ACCESS INFORMATION
--------------------------

Data License: Data is Copyright Authors above, all rights reserved

Other Rights Information: We acquire the data from https://github.com/molML/DNA-origami-stability-prediction, which is publicly available.