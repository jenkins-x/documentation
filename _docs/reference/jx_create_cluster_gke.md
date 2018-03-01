---
date: 2018-03-01T09:41:11Z
title: "jx create cluster gke"
slug: jx_create_cluster_gke
url: /commands/jx_create_cluster_gke/
---
## jx create cluster gke

Create a new kubernetes cluster on GKE: Runs on Google Cloud

### Synopsis

This command creates a new kubernetes cluster on GKE, installing required local dependencies and provisions the Jenkins X platform 

Google Kubernetes Engine is a managed environment for deploying containerized applications. It brings our latest innovations in developer productivity, resource efficiency, automated operations, and open source flexibility to accelerate your time to market. 

Google has been running production workloads in containers for over 15 years, and we build the best of what we learn into Kubernetes, the industry-leading open source container orchestrator which powers Kubernetes Engine.

```
jx create cluster gke [flags]
```

### Examples

```
  jx create cluster gke
```

### Options

```
  -b, --batch-mode                          In batch mode the command never prompts for user input
      --cleanup-temp-files                  Cleans up any temporary values.yaml used by helm install [default true] (default true)
      --cloud-environment-repo string       Cloud Environments git repo (default "https://github.com/jenkins-x/cloud-environments")
      --cluster-ipv4-cidr string            The IP address range for the pods in this cluster in CIDR notation (e.g. 10.0.0.0/14)
  -n, --cluster-name string                 The name of this cluster, default is a random generated name
  -v, --cluster-version string              The Kubernetes version to use for the master and nodes. Defaults to server-specified (default "1.7.12-gke.1")
      --default-admin-password string       the default admin password to access Jenkins, Kubernetes Dashboard, Chartmuseum and Nexus
      --default-environment-prefix string   Default environment repo prefix, your git repos will be of the form 'environment-$prefix-$envName'
      --default-environments                Creates default Staging and Production environments (default true)
  -d, --disk-size string                    Size in GB for node VM boot disks. Defaults to 100GB
      --domain string                       Domain to expose ingress endpoints.  Example: jenkinsx.io
      --draft-client-only                   Only install draft client
      --enable-autoupgrade                  Sets autoupgrade feature for a cluster's default node-pool(s)
      --exposer string                      Used to describe which strategy exposecontroller should use to access applications (default "Ingress")
      --git-api-token string                The git API token to use for creating new git repositories
      --git-provider-url string             The git server URL to create new git repositories inside (default "github.com")
      --git-username string                 The git username to use for creating new git repositories
      --headless                            Enable headless operation if using browser automation
      --helm-client-only                    Only install helm client
  -h, --help                                help for gke
      --http                                Toggle creating http or https ingress rules (default true)
      --keep-exposecontroller-job           Prevents Helm deleting the exposecontroller Job and Pod after running.  Useful for debugging exposecontroller logs but you will need to manually delete the job if you update an environment
      --labels string                       The labels to add to the cluster being created such as 'foo=bar,whatnot=123'. Label names must begin with a lowercase character ([a-z]), end with a lowercase alphanumeric ([a-z0-9]) with dashes (-), and lowercase alphanumeric ([a-z0-9]) between.
      --local-cloud-environment             Ignores default cloud-environment-repo and uses current directory 
      --local-helm-repo-name string         The name of the helm repository for the installed Chart Museum (default "releases")
  -m, --machine-type string                 The type of machine to use for nodes
      --namespace string                    The namespace the Jenkins X platform should be installed into (default "jx")
      --no-brew                             Disables the use of brew on MacOS to install dependencies like kubectl, draft, helm etc
      --num-nodes string                    The number of nodes to be created in each of the cluster's zones
  -p, --project-id string                   Google Project ID to create cluster in
      --register-local-helmrepo             Registers the Jenkins X chartmuseum registry with your helm client [default false]
      --skip-login                          Skip Google auth if already logged in via gloud auth
      --timeout string                      The number of seconds to wait for the helm install to complete (default "6000")
      --tls-acme                            Used to enable automatic TLS for ingress
      --verbose                             Enable verbose logging
  -z, --zone string                         The compute zone (e.g. us-central1-a) for the cluster
```

### SEE ALSO

* [jx create cluster](/commands/jx_create_cluster/)	 - Create a new kubernetes cluster

###### Auto generated by spf13/cobra on 1-Mar-2018
