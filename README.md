# GPT-5-Research
An exploration of the capabilities of GPT-5

## Overview
This repo shows a few examples for capability testing the GPT-5 model on Azure.   

## Setup
This project requires access to an Azure OpenAI resource to run the gpt-5 model.  At the [model catalog](https://ai.azure.com/explore/models), you will need to deploy the **gpt-5** model.  Then copy the .env.template file to a new file called .env, and update the .env file with the endpoint (and the deployment name if you change from the default).  You will also need to supply either an API key or use Microsoft Entra ID (formerly called Azure Active Directory) authentication.  We strongly recommend Microsoft Entra ID authentication for greater security.  To set it up, see https://learn.microsoft.com/azure/ai-services/openai/how-to/managed-identity.  Don't forget that you may need to run "az login" to refresh your credentials.  

Finally, use the following commands in a python environment (such as an Anaconda prompt window) to set up your environment.  This creates and activates an environment and installs the required packages.  For subsequent runs after the initial install, you will only need to activate the environment and then run the python script.  

### First run
```
conda create --name gpt5Research -y
conda activate gpt5Research

pip install -r requirements.txt
jupyter notebook gpt5Research.ipynb
```

### Subsequent runs
```
conda activate gpt5Research
jupyter notebook gpt5Research.ipynb
```
