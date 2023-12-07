# Lab3-BackDoor-Attacks
"Lab3-BackDoor-Attacks" project, a comprehensive exploration and solution for identifying and mitigating backdoor attacks in neural networks, specifically focusing on BadNets trained on the YouTube Face dataset.

---

# README for ML for Cyber Security Lab 3

## Overview

This repository contains the files for the third laboratory exercise in the Machine Learning for Cyber Security course. The main objective of this lab is to implement and analyze a backdoor detector for BadNets using pruning defense. The lab involves experimenting with different threshold levels for pruning to repair a model that has been compromised by a backdoor attack.

## File Descriptions

1. **ML for Cyber Security Lab 3.png**: 
   - This image is a graphical representation of the Attack Success Rate vs Accuracy plot while varying degrees of pruning

2. **README.md**: 
   - This file provides an overview and instructions for the repository. It's the file you are currently reading.

3. **ar8002Report on the Implementation and Analysis of a Backdoor Detector for BadNets Using Pruning Defense - Lab3 .pdf**:
   - This comprehensive report details the implementation process, analysis, and findings of the pruning defense against BadNets in the lab. It includes methodology, results, and discussion sections.

4. **ar8002_ML_for_CyberSec_Lab3.ipynb**:
   - A Jupyter notebook containing the executable code, annotations, and results for the lab. This interactive format allows for a step-by-step execution and observation of the pruning process and its effects on the model.

5. **ar8002_ml_for_cybersec_lab3.py**:
   - The Python script version of the Jupyter notebook. This script can be run in environments where Jupyter is not available or for batch processing.

6. **pruning_data.csv**
   - This dataset includes the data saved plotting the results after pruning the model. It might contain information on different parameters or metrics observed during the pruning process.

7. **repaired_model_threshold_[threshold_value].h5**:
   - These files (`repaired_model_threshold_10.h5`, `repaired_model_threshold_2.h5`, `repaired_model_threshold_20.h5`, `repaired_model_threshold_4.h5`) are the saved models after applying different pruning thresholds ( 2, 4, 10, 20). Each file represents a model repaired to a specific threshold level, which can be used for further analysis or comparison.


---

Feel free to modify this template to better fit the specifics of your project and to provide any additional instructions or information that might be relevant.
