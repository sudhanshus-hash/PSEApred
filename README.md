# PSEApred: Identification of Proteins Secreted by Malaria Parasite into Erythrocyte Using SVM and PSSM Profiles

PSEApred is a computational web server developed for predicting proteins secreted by the malaria parasite Plasmodium falciparum into infected erythrocytes.

The tool helps identify parasite-secreted proteins that may be involved in host-cell remodeling, parasite survival, immune evasion, malaria pathogenesis, and potential drug or vaccine target discovery. PSEApred uses support vector machine-based models trained on amino acid composition, dipeptide composition, split-composition features, pseudo amino acid composition, and evolutionary information from PSSM profiles.

Web Server: http://www.imtech.res.in/raghava/pseapred/



## Citation

Verma, R., Tiwari, A., Kaur, S., Varshney, G. C., and Raghava, G. P. S. Identification of proteins secreted by malaria parasite into erythrocyte using SVM and PSSM profiles. BMC Bioinformatics, 9, 201, 2008.
https://doi.org/10.1186/1471-2105-9-201

This tool and dataset is also available on Zenodo at 



## About the Research

Plasmodium falciparum secretes several proteins into infected red blood cells during malaria infection. These secreted proteins help the parasite survive inside the host cell, remodel the erythrocyte, alter membrane rigidity and permeability, support cytoadherence, and evade host immunity.

Identifying secretory proteins of malaria parasites is important because these proteins can serve as potential drug targets, vaccine candidates, and markers for understanding malaria pathogenesis.

Earlier methods mainly depended on known export motifs such as PEXEL or VTS. However, many experimentally known secreted proteins do not contain these motifs, suggesting that multiple secretion pathways may exist. PSEApred was developed as a general sequence-based method that does not depend only on a single conserved motif.

Data Compilation: The study used a non-redundant dataset of 252 secretory and 252 non-secretory Plasmodium falciparum proteins. Secretory proteins were collected from literature and included Rifins, Stevors, PfEMP1 proteins, experimentally validated secretory proteins, REX proteins, PIESPs, clag9, Sbp1, and Maurer’s cleft-associated proteins. Non-secretory proteins were collected from Swiss-Prot and PlasmoDB.

Methodology: PSEApred uses support vector machine models trained on sequence-derived features and evolutionary information. The study tested amino acid composition, dipeptide composition, split amino acid composition, split dipeptide composition, pseudo amino acid composition, and PSSM profiles generated using PSI-BLAST.



## Key Features

### 1. Malaria Secretory Protein Prediction

Predictive Modeling: Allows users to submit Plasmodium falciparum protein sequences and predict whether they are secretory or non-secretory.

Organism-Specific Prediction: The tool was developed specifically for malaria parasite proteins, because general eukaryotic secretory protein predictors may fail for Plasmodium falciparum.

Motif-Independent Prediction: PSEApred does not depend only on PEXEL/VTS motifs, making it useful for proteins secreted through possible alternative pathways.



### 2. Composition-Based SVM Models

Amino Acid Composition Model: The amino acid composition-based SVM model achieved up to 85.65% accuracy with MCC 0.72.

Dipeptide Composition Model: The dipeptide composition-based SVM model achieved 86.45% accuracy with MCC 0.74.

Split Amino Acid Composition Model: The split amino acid composition model divided proteins into N-terminal, C-terminal, and middle regions and achieved around 86.40% accuracy with MCC 0.74.

Split Dipeptide Composition Model: The split dipeptide composition model achieved 88.22% accuracy with MCC 0.77.

Pseudo Amino Acid Composition Model: PseAAC-based models also performed well, but were less accurate than the PSSM-based model.



### 3. PSSM-Based Evolutionary Model

Evolutionary Information: PSEApred uses Position-Specific Scoring Matrix profiles generated from PSI-BLAST to capture evolutionary information.

Best Model: The PSSM-based SVM model achieved the highest performance.

Performance: The best PSSM-based model achieved 92.66% accuracy with MCC 0.86.

High-Specificity Prediction: The PSSM-based model could correctly predict about 73% secretory proteins at 100% specificity.

Importance: This study showed that evolutionary information provides more predictive power than single-sequence composition alone.



### 4. Integrated Web-Bench

Sequence Submission: Users can submit protein sequences for prediction.

Prediction Output: The server predicts whether the submitted sequence is a secretory or non-secretory protein.

SVM-Based Backend: The tool uses support vector machine models for classification.

PSSM-Based Prediction: The most accurate model uses PSI-BLAST-generated PSSM profiles.

User-Friendly Interface: PSEApred provides an online platform for malaria researchers to analyze Plasmodium falciparum proteins.



## Applications

Malaria Secretome Prediction: PSEApred can help identify Plasmodium falciparum proteins secreted into infected erythrocytes.

Drug Target Discovery: Secretory proteins may be involved in parasite survival and host-cell remodeling, making them potential drug targets.

Vaccine Candidate Screening: Secreted and erythrocyte-exported proteins may serve as useful candidates for malaria vaccine development.

Host-Parasite Interaction Studies: The tool can assist in studying how malaria parasites modify host red blood cells.

Functional Annotation: PSEApred can support annotation of hypothetical Plasmodium falciparum proteins.

Malaria Pathogenesis Research: The prediction of exported proteins can help researchers understand parasite virulence, cytoadherence, and immune evasion mechanisms.



## Contact and Authors

Prof. G.P.S. Raghava 

Email: raghava@iiitd.ac.in

Department of Computational Biology, Indraprastha Institute of Information Technology (IIIT-Delhi), New Delhi, India.

## Support
This work was supported by the Council of Scientific and Industrial Research and the Department of Biotechnology, Government of India.

