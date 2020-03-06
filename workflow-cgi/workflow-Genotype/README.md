# Steps

**Building the SeqDB-import file -> Steps 1 to 6.**

## 0-scanner-labid (4 attributes)

The attributes are {Postion, Tube, Container Name, labid*} <p>

1. Postion, Tube, Container Name comes from the tracx scanner file and is
   exported as a .csv file.
2. Labid needs to be added manually


| Postion       | Tube           | Container Name   | labid*|
| ------------- |:-------------:| -----:|-----:|
| A01     | 4025804078 | 3000142931 | x1 | 
| A02     | 4025804079 | 3000142931 | x2 | 


## 1-scanner-sepnr (4 attributes +1 attributes)

The new attributes is {sepnr*} that can be found at the tube with
scat that arrived at NRM. <p>


| Postion       | Tube           | Container Name   | labid*| sepnr*|
| ------------- |:-------------:| -----:|-----:|-----:|
| A01     | 4025804078 | 3000142931 | x1 | sep1234567 |
| A02     | 4025804079 | 3000142931 | x2 | sep1234568 | 



## 2-genotype (5 attributes +16 attributes )

Genotyping result from the analysis is added. The new attributes are {MU09-1,MU09-2,MU10-1,MU10-2,MU05-1,MU05-2,MU23-1,MU23-2,MU51-1,MU51-2,MU59-1,MU59-2,G10L-1,G10L- 2,MU50-1,MU50-2} <p>



| Postion       | Tube           | Container Name   | labid*| sepnr*| MU09-1       |  MU09-2            | MU10-1   | MU10-2  | MU05-1   | MU05-2  | MU23-1 | MU23-2 | MU51-1   | MU51-2  | MU59-1 | MU59-2  |
| ------------- |:-------------:| -----:|-----:|-----:| ------------- |:-------------:| -----:|-----:| -----:   | -----: | -----:      |  -----:| -----:  | -----: | -----: | -----: |
| A01     | 4025804078 | 3000142931 | x1 | sep1234567 | 104 | 116 | 135 | 151 | 125   | 125  |0  |  0 | 0   | 0 | 0 | 0 |
| A02     | 4025804079 | 3000142931 | x2 | sep1234568 | 116 | 120 | 151 | 151 | 127   | 127  |0  |  0 | 0   | 0 | 0 | 0 |


## 3-rovbase-info (21 attributes + 7 attributes)

The new attributes are {Species, Sex, date, Latitude (WGS84), Longitude (WGS84), Municipal, County}<p>


| Postion       | Tube           | Container Name   | labid*| sepnr*| MU09-1       |  MU09-2            | MU10-1   | MU10-2  | MU05-1   | MU05-2  | MU23-1 | MU23-2 | MU51-1   | MU51-2  | MU59-1 | MU59-2  |
| ------------- |:-------------:| -----:|-----:|-----:| ------------- |:-------------:| -----:|-----:| -----:   | -----: | -----:      |  -----:| -----:  | -----: | -----: | -----: |
| A01     | 4025804078 | 3000142931 | x1 | sep1234567 | 104 | 116 | 135 | 151 | 125   | 125  |0  |  0 | 0   | 0 | 0 | 0 |
| A02     | 4025804079 | 3000142931 | x2 | sep1234568 | 116 | 120 | 151 | 151 | 127   | 127  |0  |  0 | 0   | 0 | 0 | 0 |


## 4-import_to_beta

1. Drop the labid and sepnr column as they are not needed in the importer<p>
2. Import this file to [seqdb-beta](https://seqdb-beta.dina-web.net/)
3. Check import in the [seqpublic-beta](https://seqpublic-beta.dina-web.net/)





| Postion       | Tube           | Container Name   |  MU09-1       |  MU09-2            | MU10-1   | MU10-2  | MU05-1   | MU05-2  | MU23-1 | MU23-2 | MU51-1   | MU51-2  | MU59-1 | MU59-2  |
| ------------- |:-------------:| -----:|-----:| :-------------:| -----:|-----:| -----:   | -----: | -----:      |  -----:| -----:  | -----: | -----: | -----: |
| A01     | 4025804078 | 3000142931 | 104 | 116 | 135 | 151 | 125   | 125  |0  |  0 | 0   | 0 | 0 | 0 |
| A02     | 4025804079 | 3000142931 | 116 | 120 | 151 | 151 | 127   | 127  |0  |  0 | 0   | 0 | 0 | 0 |


## 5-import_to_production

**if step 4 is ok then**
1. Import this file to [seqdb](https://seqdb.nrm.se)
2. Check import in the [seqpublic](https://seqpublic.nrm.se/) 




| Postion       | Tube           | Container Name   |  MU09-1       |  MU09-2            | MU10-1   | MU10-2  | MU05-1   | MU05-2  | MU23-1 | MU23-2 | MU51-1   | MU51-2  | MU59-1 | MU59-2  |
| ------------- |:-------------:| -----:|-----:| :-------------:| -----:|-----:| -----:   | -----: | -----:      |  -----:| -----:  | -----: | -----: | -----: |
| A01     | 4025804078 | 3000142931 | 104 | 116 | 135 | 151 | 125   | 125  |0  |  0 | 0   | 0 | 0 | 0 |
| A02     | 4025804079 | 3000142931 | 116 | 120 | 151 | 151 | 127   | 127  |0  |  0 | 0   | 0 | 0 | 0 |


## 6-imported
The final step, save the imported file in this folder


