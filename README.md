# SCOMD: Misconfiguration Detection for AWS Serverless Computing

We provide the used dataset, code of our tool SCOMD, and evaluation data.


## Used dataset

This part is saved in the directory "Dataset", including:
- The directory "configuration files-real": 733 real-world configuration files with 701 configuration files from AWS SAR and 32 configuration files from GitHub.
    - They are used to conduct a study in Section 3 and learn the knowledge of our tool SCOME.
- The directory "configuration files-office": 10 configuration file examples from official documentation.
    - They are used to learn the knowledge of our tool SCOME.



## Code of our tool SCOME

The required libaries in our tool are recoreded in the file "requirement.txt". 

#### Data collection, data convertion, and knowledge generation
    - The learned knowledge is saved in the directory "knowledge".
    - The code file "AWSupdate_data.ipynb" can learn the knowledge about configuration resource types, configuration entries, and configuration entry values.
    - The code file "AWSRuleMining.ipynb" can learn the knowledge about coarse-grained and fine-grained configuration denpendencies.
    - The code file "GeneralMethod.py" contains some general method implementation.

#### Misconfiguration Detection
    - The code file "approachAWS.ipynb" conducts misconfiguration detection for a tested configuration file.
    - The knowledge data can be read only once, and then the tests are constantly carried out on the configuration file to be tested.




## Evaluation data

- Experimental evaluation 1 for 70 real-world configuration problems that are newly selected. 
    - From TEST1.yaml to TEST70.yaml. The specific links are provided in the file "realworld problem information.xlsx".

- Experimental evaluation 2 for 35 injected misconfigurations from 20 correct configuration files that are newly selected.
    - The directory "correct file" includes 20 correct configuration files.
    - From EvaluationFile1.yaml to EvaluationFile20.yaml. The specific links and corresponding injected strategies are provided in the file "injected misconfiguration information.xlsx"
