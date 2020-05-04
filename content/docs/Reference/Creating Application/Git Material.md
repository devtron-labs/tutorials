---
title: Git Material
weight: 1
bookToc: true
---

# Git Material
Git material is used to manage the source code repositories of your application.

<br />

![git Material](../../git_materia1.jpg "Adding multiple git materials")

<br />

## Multi Git/Checkout Path

Checkout path is directory under which your code is pulled for that repository. It is independent of Multi Git, even while using single Git Repository you can provide the Git Checkout Path.


<br />
![alt text](../../git_material2.jpg "Adding multiple git materials")

<br />

In the given example, if the configuration files of the repository are kept in some other Git Repository and source code is kept in the given Git Repository, the path of the repository where Configuration files are kept will be given in `Multi Git Checkout Path` so that your Docker File can use the Configuration files cloned from the other Git Repository.


If any changes are made to the source code repository or the repository which contains the configuration files then the CI will be triggered and the image file of both the repositories will be built and pushed to the ECR repository.


