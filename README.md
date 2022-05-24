# DTI-Network

DTI-Network is updated version of Neural integration of neighbor information from a heterogeneous network for discovering new drug-target interactions

# Requirements
- Tensorflow == 1.14.0
- Tflearn
- Sklearn
- Numpy


# How to use

1. First create a new conda environment
```
conda create -n dti python=3.6
```
![Screenshot_1](https://user-images.githubusercontent.com/23219577/170072143-643faa58-9cd8-4bec-9585-bf48535f9311.png)

2. Activate conda environment

```
conda activate dti
```
![Screenshot_2](https://user-images.githubusercontent.com/23219577/170072406-2bd69eca-c6dc-4b92-9541-ed709ffff980.png)

3. Install requirements

```
pip install -r requirements.txt
```
![Screenshot_3](https://user-images.githubusercontent.com/23219577/170072584-c44c7bf4-7cbb-4723-859a-3647016d0b1d.png)

4. Start Training

```
python DTI-Network.py -s 3000
```
![Screenshot_4](https://user-images.githubusercontent.com/23219577/170072812-3fcd4f36-3053-4056-9943-074ed2241f55.png)

-s parameter is optional. Default value is 3000. It means number of step that you want to train.


# Data Description
## data/ directory
- drug.txt: list of drug names
- protein.txt: list of protein names
- disease.txt: list of disease names
- se.txt: list of side effect names
- drug_dict_map: a complete ID mapping between drug names and DrugBank ID
- protein_dict_map: a complete ID mapping between protein names and UniProt ID
- mat_drug_se.txt : Drug-SideEffect association matrix
- mat_protein_protein.txt : Protein-Protein interaction matrix
- mat_protein_drug.txt : Protein-Drug interaction matrix
- mat_drug_protein.txt : Drug_Protein interaction matrix (transpose of the above matrix)
- mat_drug_protein_remove_homo.txt: Drug_Protein interaction matrix, in which homologous proteins with identity score >40% were excluded (see the paper).
- mat_drug_drug.txt : Drug-Drug interaction matrix
- mat_protein_disease.txt : Protein-Disease association matrix
- mat_drug_disease.txt : Drug-Disease association matrix
- Similarity_Matrix_Drugs.txt : Drug similarity scores based on chemical structures of drugs
- Similarity_Matrix_Proteins.txt : Protein similarity scores based on primary sequences of proteins Note: drugs, proteins, diseases and side-effects are organized in the same order across all files, including name lists, ID mappings and interaction/association matrices.

# Contributors

- Mert Daloğlu 20160808046
- Ceren Keklil 20170808019
- İbrahim Masmanacı 20170808058
