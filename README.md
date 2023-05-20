# She Code Africa Cloud School Program Final Project
Using Terraform to provision AKS,ACR and MSSQL database to deploy full stack application on kubernetes
![Architecture](https://github.com/maqamylee0/SheCodesFullstackAppDevops/blob/main/Add%20a%20heading%20(5).png)
## About 
This is a final project for the She cloud Africa Cloud School Program 2023.

It is a fullstack project that pull data from a database and displays on the website.
The project contains two text files and should translate to the main.tf and node_mssql.yaml file.
Due to the size limit of github, i decided to upload them as text files.


## Tools Used
- Terraform
- Azure Kubernetes Sevice
- Azure Container Registry
- Ms-SQL database
- Docker
- Node JS
- ejs templating

## How it Works

1. The app is containerised using docker and its image is sent Azure Container Registry.

2. The image is then pulled by the Azure kubernetes Service and deployed.

## How it was set up.

1. Used terraform to provision the Azure Container Registry, Azure kubernetes Cluster, and MS-SQL database.
2. Created an app that queries the MS-SQL database.
3. Created a docker file and built an image of the app.
4. Pushed the image to Azure Container Registry.
5. Used a yaml file to deploy the app on Azure Kubernetes Service

## How to run the project.

1. Clone project
  ```
  git clone https://github.com/maqamylee0/SheCloudSchoolDevOps
  
  ```
2. Rename files
  ``` 
  Rename files accordingly to main.tf intead of maintf.txt and node_mssql.yaml instead of node_mssqlyaml.txt
  
  ```
  
3. Provision Resources using terraform
```

terraform  apply -auto-aprove

```
4. Containerise and push image to ACR
 App project [repository](https://github.com/maqamylee0/SheCodesFullstackAppDevops)

```
docker push <loginserver>/<repositoryname>

```
5. Use yaml file to create deployment.

```
kubectl apply -f node_mssql.yaml 

```
7. Get External IP of the app

```
kubectl get svc

```

