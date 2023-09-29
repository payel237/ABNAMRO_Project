mortgage_defaulter
This repository contains code and instructions for deploying a mortgage default prediction model. Follow the steps below to set up and deploy the model.

Step 1: Clone the Repository
Copy the shared codebase to your desired folder:

bash
Copy code
git clone <repository_url>
cd mortgage_defaulter
Step 2: Set Up Virtual Environment
Create a virtual environment in the root folder using Visual Studio Code or command line:

bash
Copy code
python -m venv .venv
Activate the virtual environment:

On Windows:

bash
Copy code
.venv\Scripts\activate
On macOS/Linux:

bash
Copy code
source .venv/bin/activate
Step 3: Install Dependencies
Run the shell script to install all dependencies:

bash
Copy code
sh src/utils/setup_env.sh
Step 4: Execute the Pipeline
Navigate to the source code folder and execute the pipeline to run data preprocessing, model training, registration, and inference:

bash
Copy code
cd src/utils
sh pipeline.sh
The pipeline will perform the following tasks:

Run unit tests to ensure code quality and correctness.
Process data for the model.
Train the model and record metrics.
Register the model in the MLflow model registry.
Promote the model to a staging environment.
Migrate the model to production.
Additional Information
Unit tests: Passed successfully!
MLOPS pipeline started in Dev and Production environments.
Data processing, model training, and registration completed.
Model promotion to staging and production environments.
Deployment in production finished successfully!
The mortgage default prediction model is now deployed and ready for use in a production environment.

For further information or troubleshooting, refer to the code and documentation in this repository.




