# CMPE-172 Lab 10 Notes

For this lab, I followed the instructions in the lab manual and edited the code as given on canvas. The first part of the lab(CI Workflow) was simple enough and I was able to complete that part with no problems at all as the workflow completed on my first try. The second part of the lab(CD Workflow) was a bit more trouble as I was confused at the instructions for what to put in the values part of the Github Action Secrets. I was able to put the project id from the json file downlaoded after creating the google service account, but I was incorrectly putting the key id or the key value in the GKE_SA_KEY value section. This led me to getting the error "unexpected token x in json at position 0" under the run github-action-workflow section of the workflow. After trying different values and re-reading the instructions, I copied the entire contents of the json file and this led to the action file working properly and deploying on GKE. I ended up just re-running the jobs whenever the workflow failed which is why I ended up having only one release at completion of the lab. Once the jobs were succcessful, I created an ingress load balancer and then clicked the frontend link which redirected me to the gumball machine webpage. I was not able to capture screenshots of my workflow while still running as I kept getting the json error and was surprised when my error stppped. The following screenshots show my process in completing the lab:

## Part 1: CI Workflow
![CIWorkflow](https://github.com/Khalsa23/spring-gumball/blob/main/images/CI%20Workflow.png "CIWorkflow")

## Part 2: CD Workflow
### GKE Service Accounts 
![ServiceAccount](https://github.com/Khalsa23/spring-gumball/blob/main/images/ServiceAccount.png "ServiceAccount")
![ServiceAccountKey](https://github.com/Khalsa23/spring-gumball/blob/main/images/ServiceAccountKey.png "ServiceAccountKey")

### Github Action Secrets
![GithubSecrets](https://github.com/Khalsa23/spring-gumball/blob/main/images/GithubSecrets.png "GithubSecrets")

### Kubernetes Cluster
![Cluster](https://github.com/Khalsa23/spring-gumball/blob/main/images/Cluster.png "Cluster")

### Github Releases
![Releases](https://github.com/Khalsa23/spring-gumball/blob/main/images/Releases.png "Releases")

### Github Action Workflows
![Workflows](https://github.com/Khalsa23/spring-gumball/blob/main/images/Workflows.png "Workflows")
![CDWorkflow](https://github.com/Khalsa23/spring-gumball/blob/main/images/CD%20Workflow.png "CDWorkflow")

### Kubernetes Workload
![Workloads](https://github.com/Khalsa23/spring-gumball/blob/main/images/Workloads.png "Workloads")

### Kubernetes Services and Ingress
![Services](https://github.com/Khalsa23/spring-gumball/blob/main/images/Services.png "Services")
![CreatingIngress](https://github.com/Khalsa23/spring-gumball/blob/main/images/CreatingIngress.png "CreatingIngress")
![Ingress](https://github.com/Khalsa23/spring-gumball/blob/main/images/Ingress.png "Ingress")

### Gumball Web Page
![GumballWebPage](https://github.com/Khalsa23/spring-gumball/blob/main/images/GumballWebPage.png "GumballWebPage")



