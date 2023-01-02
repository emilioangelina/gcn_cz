# GCN_Cz

***

## Graph neural networks and molecular docking as two complementary approaches for virtual screening: a case study on Cruzain

***

This GCN was build upon the original implementation by Ryu et al. (http://github.com/seongokryu/augmented-gcn)

For the moment, the GCN is implemented in tensorflow 1. A conda environment (gcn_env.yml) is provided with the requiered dependecies already instaled (tensorflow-gpu, pandas, scikit-learn, rdkit, etc). 

### 1. Clone the repository

> git clone https://github.com/emilioangelina/gcn_cz.git

### 2. Import conda environment: 

> conda env create -f gcn_env.yml

### 3. Activate the conda environment

> conda activate tf1

### 4. Convert SMILES to 2D graphs 

Files containing the compounds SMILES and activity labels are provided in compressed files AID1478_train-zip and AID1478_test.zip.
Uncompress the zip files:

> unzip AID1478_train.zip

> unzip AID1478_test.zip

Run the script smilesToGraph_mod2 to generate the graphs from train and test smiles. 

> python smilesToGraph_mod2.py AID1478_train 10000 1

> python smilesToGraph_mod2.py AID1478_test 10000 1

### 5. Train the GCN 

> python augmented_GCN_custom_4classPred.py 










