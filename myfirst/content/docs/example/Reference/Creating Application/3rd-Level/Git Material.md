---
title: Git Material
weight: 1
---
# Git Material
Git material is used to put the source codes of your file which needs to be compiled.

![alt text](/img/git-material.PNG "Adding multiple git materials")


## Multi Git/Checkout Path
Consider a scenario where the source code of the application is present in one repository but the configuration files for that application exist on other git repository. In such cases, checkout path can be used to provide location to the configuration files so that the docker file can use the configuration file cloned from the other repository.


![alt text](/img/combo.jpg "Adding multiple git materials")


In the above scenario,if any changes are made to the source code or the repository containing the configuration files then the CI will be triggered and the image file of both the repositories will be built and pushed to the ECR repository.