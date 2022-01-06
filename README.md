# Extracting-Time-Series-properties-of-glucose-levels-in-Artificial-Pancreas
Python 2.7 
Scikit-learn 0.21.2 
Pandas 0.25.1 
Python pickle

Steps 
1.	Read the CGM and Insulin Data using pd.read_csv().
2.	Select column named alarm in insulin dataset which has the value as 'AUTO MODE ACTIVE PLGM OFF'.
3.	Sort above data with respect to the date and time column and select the first occurrence (manual is converted to automatic).
4.	Divide the data into manual and automatic CGM data.
5.	Sub-divide both manual and automatic CGM into daytime (>=06:00:00) and nighttime (<6:00:00) data.
6.	Find the metrics to be extracted for both manual and automatic modes. The percentage times are given as :
a.	CGM > 180 mg/dL
b.	CGM > 250 mg/dL
c.	CGM >= 70 mg/dL and CGM <= 180 mg/dL
d.	CGM >= 70 mg/dL and CGM <= 150 mg/dL
e.	CGM < 70 mg/dL
f.	CGM < 54 mg/dL 
7.	Finally, the results are stored to Results.csv file. Append 1.1 in the last column of Results.csv as the Results.csv file is expected to have 2 X 19 dimension.
