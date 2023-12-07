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

Steps to run the model:
Run the code on Google Colab. All dependencies are handled.

Graphical plot of the results:
![ML for Cyber Security Lab 3](https://github.com/aneekroy/Lab3-BackDoor-Attacks/assets/10370194/b335fe08-d41b-4977-888b-ab5707d3beda)

Discussions on the efffectiveness of the Pruning on the Attack Success Rates (ASR):
"""The ineffectiveness of pruning as a defense mechanism against certain types of attacks, especially in neural networks, can be attributed to several factors:

1. **Inherent Robustness of Neural Networks**: Neural networks, particularly deep networks, are known for their redundancy and robustness. When certain channels or neurons are pruned, the network can often compensate for the loss, maintaining its function almost as before. This resilience, while beneficial for generalization and dealing with noisy inputs, can also mean that pruning does not significantly impact the network's ability to process poisoned inputs or adversarial examples.

2. **Targeted Nature of Some Attacks**: Certain attacks are crafted with the specific architecture and weights of the target neural network in mind. If the attack is designed to exploit specific vulnerabilities or features of the network, pruning might not remove these vulnerabilities. Instead, it could require a more comprehensive restructuring or retraining of the model.

3. **Insufficient Pruning**: The extent of pruning is a critical factor. If pruning is too conservative, it might not remove enough of the network's capacity to mitigate the attack. On the other hand, aggressive pruning can degrade the performance of the network on legitimate tasks. Finding the right balance is challenging and often specific to the particular model and task.

4. **Distribution Shift in Poisoned Data**: Poisoned or adversarial data often represents a significant shift from the distribution of clean data. If pruning is guided primarily by performance on clean data, it may not address the specific ways in which poisoned data manipulates the model's responses. Therefore, the pruned model might still be vulnerable to attacks crafted to exploit these distributional differences.

5. **Lack of Specificity in Pruning**: Pruning, especially when it's done uniformly or based on generic criteria like activation values, may not target the specific neurons or channels that are most influential in the adversarial context. The neurons critical for processing poisoned inputs might remain largely unaffected, leaving the network's vulnerabilities intact.

6. **Recovery of Attack Capability**: In some cases, even after pruning, the model may still be capable of learning or recovering the attack patterns during further training or fine-tuning, especially if the underlying data used for these processes is not cleansed of poisoned examples.

7. **Complexity of Neural Networks**: Modern neural networks often have millions of parameters, and the relationship between these parameters and specific model behaviors can be highly non-linear and complex. This complexity makes it difficult to predict how changes like pruning will affect the model's behavior in all scenarios, including under attack.

In conclusion, while pruning can be an effective tool for reducing model size and computational complexity, its effectiveness as a defense mechanism against attacks on neural networks is limited and can be highly dependent on the nature of the attack and the specifics of the network architecture. More comprehensive approaches might be required for robust defense against sophisticated attacks.
"""

