argoconfig
==========
Configure a Caasperli deployment through Argo CD

Current chart version is `0.1.0`

Source code can be found [here](https://github.com/hairmare/helm-caasperli)



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| appProject.clusterResourceWhitelist[0].group | string | `"*"` | API groups to whitelist |
| appProject.clusterResourceWhitelist[0].kind | string | `"*"` | API kind to whitelist |
| appProject.destinations[0].namespace | string | `"*"` | Destination namespace to allow |
| appProject.destinations[0].server | string | `"*"` | Destination server to allow |
| appProject.enabled | bool | `true` | Enable creating an AppProject resource |
| appProject.namespace | string | `"argocd"` | Namespace for AppProject resource |
| appProject.sourceRepos | list | `["*"]` | Source repos to allow |
| application.destination.namespace | string | `"caasperli"` | Target namespace of application in Argo CD |
| application.destination.server | string | `"https://kubernetes.default.svc"` | Target cluster in Argo CD |
| application.enabled | bool | `true` | Enable creating an Application resource |
| application.namespace | string | `"argocd"` | Namespace for Application resource |
| application.projectOverride | string | Fullname | Name of AppProject to install into |
| application.source.chart | string | `"caasperli"` | Name of chart in source repo |
| application.source.repoURL | string | `"https://hairmare.github.io/helm-caasperli"` | URL of sourece repo |
| application.source.targetRevision | string | `"*"` | Revision of chart in source repo to install |
| fullnameOverride | string | `""` | Override fullname |
| nameOverride | string | `""` | Override names |
