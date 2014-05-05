# An assesment of the Docker micro container

> Darrell Pratt, Architect Leader, GBS


## Executive Summary

Virtual machines have always been a large part of any sizeable development organization and their use as a means to virtualize the resources of a physical machine are well known.  A new application called Docker is turning this concept of virtualization into immediately accessible micro containers for any organization to easily tie into their workflows. This framework has grown verey rapidly with even Amazon Web Services just recently announcing support for Docker in their Elastic Cloud service.


## Problem Statement

Virtualization has helped companies make the best use of their physical hardware within data centers.  Primarily, this has been the realm of VMWare and few other built in solutions within various operating systems. Although some groups have built quite a bit of tooling around VMWare and the provisioning of images to users, there is still quite a bit of setup involved with this approach and no true method for the developer to declare which resources are needed for the image and how to separate those images based upon the application's needs. At the completion of provisioning, one still has a VM that looks like a physical machine that might be running various application servers or databases. There is no true separation of concerns with this approach. 

## Docker Background

Docker was created to solve the issue of build once, run anywhere. Docker automates the creation of a self-sufficient container that can run anywhere, but displays the same outward behaviour to the developer or ops team regardless of location. A central difference between Docker and traditional virtual machines, is that the Docker image is extremely lightweight as it has no host OS (it uses the host OS) it can be deployed and started with very minimal delay. An illustration of the difference between a traditional container and Docker is illustrated below.

![Docker vs. VMs][dockervm1]

Docker manages to scale in the sense of maintaining many images of different applications or version of those applications because of this design pattern. The container is essentialy the application and its dependent binaries and libraries. Docker is intelligent enough to only store the differential between any of these layers across the same base images.

What does this mean? For example, imagine a large Java Application which is maintained in git with a build process hosted within Jenkins.  The build process could easily take a given base Dockerfile and load a different codebase into that container, instantiate it, run a full test suite and then decommission that container. The build could do this is a completely automated fashion. These containers can also run in parallel on a host or host sharing the unchanged components between each container. This allows for scaling the number of containers with very little disk space or resources being used.  With a traditional VM infrastructure, this would require unique guest host images, which are several gigabytes in size each and take time to build and startup.  Docker makes this trivial and extremely fast.

The Docker name itself comes from the idea of shipping.  As the company explains it, shipping used to be done in a [break bulk fashion](wikiBreakBulkLink) .

## Configuration


## Image Management and Creation


## Image Linking


## Scripting Docker with Ansible


## Use Case


## Benefits


## Conclusion




[dockervm1]: https://raw.githubusercontent.com/darrellpratt/whitepapers/master/2014/images/docker_vm.jpg
[wikiBreakBulkLink] : http://en.wikipedia.org/wiki/Break_bulk_cargo

