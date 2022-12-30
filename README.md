# Deploying .Net Microservices with AKS

In this project, we're going to deploy .Net Microservices into **Kubernetes**, and move deployments to the cloud **Azure Kubernetes Services** (AKS) using **Azure Container Registry** (ACR). In the end, we will alxo perform Automated Deployments with CI/CD pipelines of **Azure DevOps** and **GitHub**.

We're going to containerize our microservices on docker environment, and push images to the Docker Hub and deploy microservices on Kubernetes. As the same setup, we are going to perform shifting to the cloud for deploying AKS (**Azure Kubernetes Services**) using ACR (**Azure Container Registry**).

We will cover additional topics as :
- Docker compose microservices
- Kubernetes components (pods, deployments, services ..)
- Zero-downtime deployments
- Using Azure resources like ACR (**Azure Container Registry**), AKS (**Azure Kubernetes Services**)
- Automate whole deployment process by writing custom pipelines with Azure DevOps and so on..

## Developping Shopping.Client Microservice

### Run Docker
<img src="/pictures/docker_run.png" title="docker run"  width="800">

### Docker commands
```
docker run -d -p 8000:80 --name myapp shoppingclient
docker tag shoppingclient dockeralexei/shoppingclient:version1
docker push dockeralexei/shoppingclient:version1
```
<img src="/pictures/docker_push.png" title="docker push"  width="800">


## Deploy Shopping.Client Microservice to **Azure App Services**

### Create Web App
<img src="/pictures/create_web_app.png" title="create web app"  width="800">

Caution : you need to specify *dockeralexei/shoppingclient:version1* instead of *dockeralexei/shoppingclient*

<img src="/pictures/create_web_app2.png" title="create web app"  width="800">
<img src="/pictures/create_web_app3.png" title="create web app"  width="800">
<img src="/pictures/create_web_app4.png" title="create web app"  width="800">

### Set Continuous Deployment
<img src="/pictures/continuous_deployment.png" title="continuous deployment"  width="800">
<img src="/pictures/continuous_deployment2.png" title="continuous deployment"  width="800">