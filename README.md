# Plane Helm Chart

This repository contains the Helm chart for deploying the Plane project using Kubernetes.

The .tgz file representing the Helm chart for this project is available in the "Deploy > Releases" section of the GitLab project.
For more details on the Plane project, visit Plane Project Page https://plane.so/.


## Installing the Helm Chart

To use this Helm chart, follow these steps:

1. Add this repository to your Kubernetes cluster as a Helm repository using the following command:


helm repo add --username <your-gitlab-username> --password <your-personal-access-token>  <your-repo-name>  https://gitlab.comwork.io/api/v4/projects/2297/packages/helm/release

Replace <your-gitlab-username> with your GitLab username and <your-personal-access-token> with your personal access token, and you <your-repo-name> with a name you choose for the repo. 

2. Update the Helm repositories:

helm repo update


3. Install the Helm release using the following command.


helm install <name-of-release> <your-repo-name>/plane-helm-chart

Replace <name-of-release> with the name you want for your Helm release, and you <your-repo-name> with the name you chose for the repo.



## Updating the Helm Chart

If you want to update the helm chart 
1. Clone the project in your local machine

2. Do the necessary updates.

3. Package the helm chart by running the following command in the root of the project:     helm package . 

4. push the image to the repo by running:
         helm cm-push  <the-created-.tgz-file> <your-repo-name>






For more information on Helm, refer to the official Helm documentation.

