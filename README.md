## Install WordPress with Helm Chart

In this How-To Document we will deploy a sample wordpress app to Kubernetes with Helm Chart. Required Files and Steps:

1. **Required Files**
      1. Deploymenet yaml files for SQL and Wordpress
      2. Helm

2. **Steps**
    1. Install Helm
    2. Init Helm Chart
    3. Configure & Deploy

## Install Helm
Use the command `sudo snap install helm --classic` to install helm (tested on ubuntu)

## Create and Deploy Helm 
Run the command to init helm 
      
      helm create wordpress-chart

this create init a helm chart required files. 

*  **Chart.yaml** describes the chart, as in it’s name, description and version.
*  **Values.yaml** is stores variables for the template files templates directory. If you have more complex deployment needs, that falls outside the default templates capability, edit the files in this directory. They are normal Go templates, Hugo (https://gohugo.io) which btw powers this blog, have a nice Go template primer (https://gohugo.io/templates/go-templates/), if you need more information on how to work with Go templates.
*  **NOTES.txt** is used to give information after deployment to the user that deployed the chart. For example it might explain how to use the chart, or list default settings, etc. For this post I will keep the default message in it.
