## aquactl commands
More info at [https://docs.aquasec.com/](https://docs.aquasec.com/)

**aquactl -h** - *Gets help*

**aquactl login** - *Logs in to run other commands*

**aquactl download all** - *Downloads the manifests (YAML files) that are used to deploy Aqua Server, Database, Gateway, Enforcer, and KubeEnforcer*

### Flags used in aquactl
* -p, -platform 
* -v, -version
* -r, -registry
* --pull-policy
* --service-account
* -n, --namespace
* --output-dir - *Directory location for outputting YAML manifest files; defaults to directory aquactl was launched from*
