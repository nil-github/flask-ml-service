[![Build Status](https://dev.azure.com/odluser254899/flask-ml-service_dev/_apis/build/status%2Fnil-github.flask-ml-service_dev?branchName=main)](https://dev.azure.com/odluser254899/flask-ml-service_dev/_build/latest?definitionId=2&branchName=main)

[![Python application test with Github Actions](https://github.com/nil-github/flask-ml-service_dev/actions/workflows/main.yml/badge.svg)](https://github.com/nil-github/flask-ml-service_dev/actions/workflows/main.yml)

Trello board:

https://trello.com/b/6S7265Lc/my-trello-board

Spreadsheet : Quarterly yearly weekly plan 

[Quarterly.yearly.weekly_plan.xlsx](https://github.com/nil-github/flask-ml-service_dev/files/14634707/Quarterly.yearly.weekly_plan.xlsx)



Architecture:

 ![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/7dcf0a80-f63c-4234-a388-7b68181cdae9)

1>Create a Github Repo containing requirements.txt and Makefile

 ![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/75f858fa-bd01-4da4-8ebd-155511a9e331)

 

2>Connect Azure Cloud Shell with Github Repo with ssh-keys 

 ![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/8eada47a-2c54-4ac8-8664-bd871da2d1da)


3>Setup Virtual Environment and activate it

 python3 -m venv ~/.flask-ml-azure

 source ~/.flask-ml-azure/bin/activate


4>Clone Github Repo to Azure Cloud Shell

 git clone git@github.com:nil-github/flask-ml-service.git


5>run make all in Azure cloud shell to download all the dependencies and test the code

 make all
![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/5dae069c-d918-4f1d-b67a-cf8c22b0c668)


6>Deploy the app to Azure App Service

 az webapp up -n seemyazureapponline15 --resource-group Azuredevops --sku F1

 ![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/75ade380-801a-494f-9888-f162cb6f533c)
 ![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/3910bd4b-a420-4b1e-b3c7-16af6f4dccf3)
 ![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/31e9ff9b-51ea-44bb-8f5f-918ea4a5fbb8)


7>Make Manual Prediction

 chmod +x make_predict_azure_app.sh

 ./make_predict_azure_app.sh

 ![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/e1f87b4b-6863-4e52-963e-2a030740582c)
 ![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/415896b9-3cb8-4543-bfc8-9853e3d570c9)


8>Run load test with locust

 pip insall locust

 locust -f locust.py
 ![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/d475c797-2021-4577-a4bc-b40b8bcf0b29)


9>Create new Azure Devops project and add the pipeline

![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/3c0b2601-57ac-4477-88f1-205056d7a28c)
![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/f244a8ae-9fa7-477f-b8b9-222266461825)
![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/aa7b60c4-b32d-47aa-ad41-a4f6e5b5fefe)
![image](https://github.com/nil-github/flask-ml-service_dev/assets/66524063/868f95bf-7b0a-4975-b2ca-217835314266)

Demo:
 https://www.youtube.com/watch?v=hu-tCO7409Q






 

 




 
 

 




 
 

