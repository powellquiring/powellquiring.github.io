---
layout: post
title: create a docker image
excerpt: Create a docker image from a docker file directory on github.
---
{{ page.excerpt }}

Have [docker hub](https://hub.docker.com/) build and store your docker images.
Create [github](https://github.com/) repository containing the Dockerfile source and any other static files needed to docker build your docker image.
Log into your [docker hub](https://hub.docker.com/) account and choose `Add Repository` > `Automated Build`.
Connect your github account to your docker hub.
Select the github docker repository.
Your docker image will be ready in a moment.
See an example here: [jekyllgithubpages](https://github.com/powellquiring/jekyllgithubpages)
I use this docker image to develop this site
