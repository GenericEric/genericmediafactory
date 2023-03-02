# bgeneric-charts
## Spin up your own media factory in Kubernetes
These charts are meant to deploy a full-on factory to manage all aspects of your self-hosted media. They utilize the *arr suite of applications for which documentation can be found [here](https://wiki.servarr.com).
\
# Assumptions
* You have a Kubernetes cluster deployed
* You have Helm installed with access to said cluster
* You have an existing PersistentVolumeClaim set up in the namespace you will deploy to that is or links to your media library
* You are okay using hostPath for config directories and download directory (you can mount a network share to this hostPath and skip using the PersistentVolumeClaim)
\

## more documentation coming soon...
