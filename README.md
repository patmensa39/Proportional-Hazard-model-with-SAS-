# Proportional-Hazard-model-with-SAS-
Fitting Proportional Hazard model with SAS 

data clinical_trial;

infile "/home/u49706966/AppliedSurvivalAnalysis/Clinical Trial.csv" dsd firstobs=2; 

input tt status group;

run;



ODS GRAPHICS On;

proc phreg;

model tt * status(0) = group;

run;

