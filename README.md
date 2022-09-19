## aquactl commands
More info at [https://docs.aquasec.com/](https://docs.aquasec.com/)

Note - **assurance** scans applications and infrastructure for potential security issues. **Enforcement** prevents (at runtime) workloads and infrastructure from performing potentially insecure operations.



**aquactl -h** *Gets help*

**aquactl login** - *Logs in to run other commands*

        aquactl login --serverUrl http://<AQUA_SERVER>:8080 \
              --user <AQUA_USER> --password <AQUA_PASS>

**aquactl stats --get-csp-stats** - *Gets enterprise stats*

**aquactl download all** - *Downloads the manifests (YAML files) that are used to deploy Aqua Server, Database, Gateway, Enforcer, and KubeEnforcer*

**aquactl image-assurance** - *This command allows you to edit image asssurance policies*

        aquactl image-assurance --get-image-assurance-policies
        
        aquactl image-assurance --create --policy-path <NewPolicyName.json>
        
        aquactl image-assurance --update --policy-path <updatedPolicyContents.json> \
        --image-assurance-id <PolicyName>

**aquactl function-assurance** - *similar to image-assurance*

**aquactl runtime-policy** - *policy for container runtimes*

**aquactl nanoenforcer** - *adds nanoenforcer as a layer of AWS Lambda or Azure Functions*
[Specific instructions are here](https://docs.aquasec.com/v6.5/platform/aquactl/aquactl-add-nanoenforcer/)



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
