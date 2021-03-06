# Open Source PaaS List

Platform as a Service simplifies and streamlines deployment.

Yes, I can use ssh+vi to manage servers. I did this since 1998, but ssh+vi is not 
a professional way to manager servers.

Yes, I know how to use configuration management (SaltStack or Ansible) to manage servers. But this misses
the streamlining effect, which you get from a PaaS solution.

PaaS are usualy using some kind of containers to execute the applications.

## Required Features

* As a software developer I want to deploy a several Django based app on one VPS.
* I don't want to run a big infrastructure, I just have one VPS. Kubernetes based solutions don't make sense for me at the moment.
* I want http. Letsencryptit support is needed.
* Documentation. The PaaS should be documented. I don't want to be the first who tries to get a Django based solution running on it.

## Dokku

Dokku copies Heroku. I guess this is very great if you want to switch from Heroku to a self-hosted solution. But this
is not my use case.

It is mostly written in Shell. I don't trust Shellscripts, but the author is maintaining it with love since several years. Looks stable.

Dokku has three ways to operate: herokuish buildscripts, Dockerfiles, Docker-Images.

First I though "herokuish buildscripts" are great, but maybe this mixes two things which don't belong together: Creating a container and running a container.

Multi-Host: No

With Dokku you can "link" an App to a database. This automatically creates a matching DATABASE_URL. 
See [Linking backing services to applications](http://dokku.viewdocs.io/dokku/deployment/application-deployment/#linking-backing-services-to-applications)
That's cool.

## Flynn

This was cool some years ago. Now there are 430 open issues, and the development has stalled.

## CapRover

[CapRover](https://github.com/caprover/caprover)

Has a web-GUI.

Written in Typescript.

Nice docs.

Nice feature [Rollback to previous Docker Image](https://caprover.com/docs/deployment-methods.html#one-click-rollback)

The docs advertise DigitalOcean, but CapRover runs on Hetzner or any other VPS.

Multi-Host: Yes (Docker Swarm)

## Tsuru

[Tsuru](https://tsuru.io/)

Written in go. Uses Docker-Swarm.

Multi-Host: Yes

# kel
[kelproject](https://github.com/kelproject) development has stalled.

# Too big

At least at the moment I think solutions based on Kubernetes are too big for me. I have only one VPS, I don't want a run a cloud.

* Rancher (RedHat)
* OpenShift
* Cloud Foundry

# Star-History

![paas-star-history](paas-star-history.png)

Source: [star-history](https://star-history.t9t.io/#caprover/caprover&flynn/flynn&tsuru/tsuru&dokku/dokku)

