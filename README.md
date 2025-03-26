
Gene expression matrix (GEM) Overview:
This gem showcases names of different genes with values that represent expression levels of various the genes in each of the BCRA samples. 

Prometheus prompts: 
- What is TSPAN gene and what does the value signify in this GEM? 
- What Could cause abnormal TSPAN expression? 

Objects: 
+ Download gene data from https://portal.gdc.cancer.gov/
+ Place in Linux working environment 
+ Create script in python that separate and place each gene name with their respective gene expression value

Task: 
- Visit https://portal.gdc.cancer.gov/ and Download data BRCA data
   - Cohort Builder --> Project --> type TCGA-BRCA
   - Select: "Available Data", Data Category: "Transcriptome profiling", Experimental Strategy: "RNAseq", & Data Type: "Gene expression quantification"
   -  Download the manifest file

-Take manifest file and uploaded to a Linux working environment
  -Create separate directory to work in
  -Copy the file to your path 
 
# Useful tools
- wget https://gdc.cancer.gov/system/files/public/file/gdc-client_2.3_Ubuntu_x64-py3.8-ubuntu-20.04.zip
- pip install

- Uncompress the manifest file 
  - Copy the gdc client to your PATH

- Use GDC client to access the data from the manifest file 
gdc-client download -m [manifest_file]

- Write python script that passes data
   +Included in this repository

-Write slurm script that tell computer what to do
   + Included in this repository
    

# Output file is named: gene_expression_simple.tsv




This project is licensed under the MIT License. 
