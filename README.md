## aquactl commands
More info at [https://docs.aquasec.com/](https://docs.aquasec.com/)

**aquactl -h** - *Gets help*

**aquactl login** - *Logs in to run other commands*

**aquactl download all** - *Downloads the manifests (YAML files) that are used to deploy Aqua Server, Database, Gateway, Enforcer, and KubeEnforcer*

### Flags used in aquactl
* -p, -platform  - *REQUIRED - platform that aqua is deployed on - i.e. kubernetes, aks, eks, gke, openshift, rancher, etc*
* -v, -version - *REQUIRED - major version of aqua to deploy*
* -r, -registry - *Docker registry containing Aqua Enterprise images; defaults to registry.aquasec.com*
* --pull-policy - *This is the Docker image pull policy; defaults to IfNotPresent*
* --service-account - *K8s service account name, defaults to aqua-sa*
* -n, --namespace  - *Kubernetes namespace; defaults to aqua*
* --output-dir - *Directory location for outputting YAML manifest files; defaults to directory aquactl was launched from*

Example usage: 
    
    aquactl download all --platform gke --version 6.5
    
    aquactl download enforcer --platform aks --version 6.5
    
s
