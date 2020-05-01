---
title: Git Material
weight: 1
bookToc: true
---

# Git Material
Git material is used to manage the source code repositories of your application.

<br>

![git Material](../../git_materia1.jpg "Adding multiple git materials")

<br>

## Multi Git/Checkout Path

Consider a scenario where the source code of the application is present in one repository but the configuration files for that application exist on other git repository. In such cases, checkout path can be used to provide location to the configuration files so that the docker file can use the configuration file cloned from the other repository.

<br>

![alt text](../../git_material2.jpg "Adding multiple git materials")

<br>

In the above scenario,if any changes are made to the source code or the repository containing the configuration files then the CI will be triggered and the image file of both the repositories will be built and pushed to the ECR repository.