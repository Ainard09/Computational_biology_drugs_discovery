# Computational_biology_drugs_discovery
## Motivations

**Drug discovery** is the process of identifying and developing new medications to treat or prevent diseases. This involves a combination of scientific research, drug design, and preclinical testing to identify molecules that have the potential to become safe and effective drugs. The process typically begins with the identification of a target molecule or biological pathway that is involved in a disease, followed by the screening of large numbers of compounds to identify those that have the desired **biological activity**. Once a promising compound has been identified, it undergoes preclinical testing to assess its safety and efficacy before proceeding to clinical trials in humans. The area of focus on this project is **Alhzeimer's disease** and working on predictive drug with high potency at IC50 to inhibit the causative enzyme.

**Acetylcholinesterase** (AChE) inhibitors are a type of drug that can be used to treat various neurological disorders by targeting the enzyme acetylcholinesterase. **Quantitative Structur-Activity Relationship** (QSAR) is a computational tool that can be used to develop models that predict the biological activity of molecules based on their chemical structure. The purpose of this project is to look into chemical structure of compounds and comparatively analyse their bioactivity potency toward targeting AChE as a potential enzyme hence, promote the continuous flow of acetylcholine (neurostransmitter responsible for cognitive activity and memory retention) in the body system.This project is highly motivated by this [[research paper]](https://peerj.com/articles/2322/).
![image](/images/image2.png)

## Dataset

A data set of inhibitors against human AChE (Target ID CHEMBL220) were compiled from the ChEMBL 20 database that is comprised of a total number of 8,502 bioactivity data points from 5,905 compounds with inhibitory concentration at 50% `(IC50)`

## Files

- `drug_discovery1.ipynb`: data collections and preprocessed jupyter notebook
- `drug_discovery_EDA2`: Lipinski descriptors calculation and data visualization
- `drug_discovery_acetylcholinesterase_descriptors_dataset`: PEDAL descriptor calculations
- `drug_discovery_modelling`: Model building with random classifier regressor

## Results

Firstly, the compounds were grouped into 3 labels; active,intermediate and inactive. This was based on the potency level in nanomolar of the compounds. The Lipinski’s rule-of-five consist of molecular weight (MW), logarithm of the octanol/water partition coefficient (ALogP), number of hydrogen bond donor (nHBDon) and number of hydrogen bond acceptor (nHBAcc); all these give the overview of the compound's druglikeness.
The Mann Whitney U Test was used to measure the statistical difference between the active group (< 1,000nM) and inactive group (> 10,000nm). All of the 4 Lipinski's descriptors exhibited **statistically significant difference** between the **actives** and **inactives**. The [PaDEL-Descriptor software](https://onlinelibrary.wiley.com/doi/10.1002/jcc.21707) calculate the molecular descriptors and fingerprints for the compounds. This gives the descriptors features needed to build a model.
