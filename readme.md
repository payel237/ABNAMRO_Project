### Mortgage_defaulter

This Folder contains code and instructions for deploying a mortgage default prediction model. Follow the steps below to set up and deploy the model.

##### Step 1:   Copy the shared codebase in desired folder. 

##### Step 2:   Setup virtual environment in root folder using visual studio code or command. 

##### Step 3: Run the shell script to install all dependencies in same root folder
```shell
ppanja@LT461206 MINGW64 ~/POC/mortgage_defaulter
$ sh src/utils/setup_env.sh
```
#####Step 4: Navigate to the source code folder & execute the pipeline to run data preprocessing, model training , registering & inferecing. 


```shell
cd src/utils
sh pipeline.sh 
```
###### Output of Pipeline

    Running unit tests
    ========================================================= test session starts =========================================================
    platform win32 -- Python 3.10.4, pytest-7.4.2, pluggy-1.3.0
    rootdir: C:\Users\ppanja\POC\mortgage_defaulter\src\utils
    plugins: typeguard-4.1.5
    collected 1 item
    
    testing.py .                                                                                                                     [100%]
    
    ========================================================== 1 passed in 0.78s ========================================================== 
    Unit tests: Passed !!
    MLOPS pipeline started in Dev
    Performing Data Processing.. 
    Data Processing Completed 
    Performing Model Training ..
    Data Processing Completed 
    Creating experiment & recording model metrics .. 
    Experiment submited & recorded model metrics 
    Model promotion is in Progress .. 
    Registered model 'model_name' already exists. Creating a new version of this model...
    2023/09/29 16:48:25 INFO mlflow.tracking._model_registry.client: Waiting up to 300 seconds for model version to finish creation. Model name: model_name, version 11
    Created version '11' of model 'model_name'.
    Model promotion completed..
    Migrating model to ..  Staging
    Model migrated to ..  Staging
    Inferecing for end user 
    C:\Users\ppanja\POC\mortgage_defaulter\.venv\lib\site-packages\sklearn\base.py:458: UserWarning: X has feature names, but RandomForestClassifier was fitted without feature names
      warnings.warn(
    Output from Model
       id_customer  age_customer  age_credit  ...  n_transactions_last_month  volume_last_month  mortgage_defaulter
    0         7327            98          97  ...                          7         282.976590                   1
    1         7340            31           5  ...                         15         270.036026                   1
    2         7355            48         157  ...                         13         189.150910                   1
    3         7360            77         121  ...                          9         146.414624                   1
    4         7372            77         219  ...                          7         111.098443                   1
    
    [5 rows x 10 columns]
    MLOPS pipeline run is finished in Dev
    
    MLOPS pipeline started in Production
    Performing Data Processing.. 
    Data Processing Completed 
    Performing Model Training .. 
    Data Processing Completed 
    Creating experiment & recording model metrics .. 
    Experiment submited & recorded model metrics 
    Model promotion is in Progress .. 
    Registered model 'model_name' already exists. Creating a new version of this model...
    2023/09/29 16:48:35 INFO mlflow.tracking._model_registry.client: Waiting up to 300 seconds for model version to finish creation. Model name: model_name, version 12
    Created version '12' of model 'model_name'.
    Model promotion completed..
    Migrating model to ..  Production
    Model migrated to ..  Production
    Inferecing for end user
    C:\Users\ppanja\POC\mortgage_defaulter\.venv\lib\site-packages\sklearn\base.py:458: UserWarning: X has feature names, but RandomForestClassifier was fitted without feature names
      warnings.warn(
    Output from Model
       id_customer  age_customer  age_credit  ...  n_transactions_last_month  volume_last_month  mortgage_defaulter
    0         7327            98          97  ...                          7         282.976590                   1
    1         7340            31           5  ...                         15         270.036026                   1
    2         7355            48         157  ...                         13         189.150910                   1
    3         7360            77         121  ...                          9         146.414624                   1
    4         7372            77         219  ...                          7         111.098443                   1
    
    [5 rows x 10 columns]
    MLOPS pipeline run is finished in Production
    
    Deployment in Production finished sucessfully!!!
    (.venv)
