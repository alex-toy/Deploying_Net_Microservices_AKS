# Deploying .Net Microservices with AKS

In this project, we're going to deploy .Net Microservices into **Kubernetes**, and move deployments to the cloud **Azure Kubernetes Services** (AKS) using **Azure Container Registry** (ACR). In the end, we will alxo perform Automated Deployments with CI/CD pipelines of **Azure DevOps** and **GitHub**.

We're going to containerize our microservices on docker environment, and push images to the Docker Hub and deploy microservices on Kubernetes. As the same setup, we are going to perform shifting to the cloud for deploying AKS (Azure Kubernetes Services) using ACR (Azure Container Registry).

We will cover additional topics as :
- Docker compose microservices
- Kubernetes components (pods, deployments, services ..)
- Zero-downtime deployments
- Using Azure resources like ACR (**Azure Container Registry**), AKS (**Azure Kubernetes Services**)
- Automate whole deployment process by writing custom pipelines with Azure DevOps and so on..

## Shopping.Client

### Run Docker
<img src="/pictures/docker_run.png" title="docker run"  width="800">

### Docker commands
```
docker run -d -p 8000:80 --name myapp shoppingclient
docker tag shoppingclient dockeralexei/shoppingclient:version1
docker push dockeralexei/shoppingclient:version1
```
<img src="/pictures/docker_push.png" title="docker push"  width="800">