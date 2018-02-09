---
title: Minikube
category: Installation
order: 1
toc: true
---

## Install Minikube

The quickest way to get started is to install Minikube using Homebrew:

    brew cask install minikube
    brew install kubernetes-helm

Then install [Docker for Mac](https://docs.docker.com/docker-for-mac/install/). This contains the HyperKit binary you will need to run Kubernetes on your Mac

To start Kubernetes:

    minikube start --vm-driver hyperkit --memory 4028

## Configure Minikube

Once Kubernetes is started, yoiu need to enable the ingress addon (run once after installation):

    minikube addons enable ingress


## Setup Jenkins X

Then ensure that Helm is initialized on your Kubernetes cluster by running:

    helm init

Helm will initialize its services on the cluster. You can continue when the `tiller` service is in the `Running` status

    kubectl get pods --namespace kube-system | grep 'tiller'
    tiller-deploy-7594bf7b76-5vh8s          1/1       Running   0          1m

To install Jenkins X:

    jx install

On every machine you interact with Jenkins X you will need to run the following command to interact with Jenkins X using the `jx` command line:

    jx init
