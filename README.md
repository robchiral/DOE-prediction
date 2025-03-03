## Genetic evidence informs the direction of therapeutic modulation in drug development

### Drug dataset
* **drug_mechanisms.csv**: contains unified drug mechanisms from ChEMBL 35, DrugBank 5.1.13, and Guide to PHARMACOLOGY 2024.4.
* **x_to_doeid.csv**: contains conversions between internal drug IDs and ChEMBL IDs/DrugBank IDs/PubCHEM CIDs

### Notebooks
* **Drug data.ipynb**: code used to clean ChEMBL, DrugBank, Guide to PHARMACOLOGY, and Open Targets datasets
* **Drug analysis.ipynb**: code used to analyze drug data
* **Gene models.ipynb**: code used to train gene-level models
* **Gene-disease models.ipynb**: code used to train gene-disease-specific models

> [!NOTE]
> We cannot share some of the raw files needed to run these files as they require registration to obtain (e.g., DrugBank, OMIM) or are too large to host here (e.g., GenePT). Please download these files yourself.

### Predictions
* **druggability.csv**: contains overall and DOE-specific druggability predictions for 19,450 protein coding genes
* **doe.csv**: contains isolated DOE predictions for 19,450 protein coding genes
* **gene_disease_doe.csv**: contains isolated DOE predictions for 662,769 gene-disease pairs

> [!IMPORTANT]
> Because DOE models were trained among druggable models, we cannot guarantee good performance among non-druggable genes. Thus, for **doe.csv** and **gene_disease_doe.csv**, we recommend filtering for rows where **"Likely druggable" = 1** (i.e., known druggable genes and genes with predicted druggability > 0.5). 

> [!TIP]
> For **gene_disease_doe.csv**, we also recommend filtering for predictions with multiple lines of genetic evidence. In this file, "Non-zero features" column is the number of non-zero genetic features (excluding LOEUF) and "Non-zero AF bins" is the number of allele frequency (AF) bins (common, rare, ultrarare) with non-zero features.

