# bgeneric-charts
## Spin up your own media factory in Kubernetes
These charts are meant to deploy a full-on factory to manage all aspects of your self-hosted media. They utilize the *arr suite of applications for which documentation can be found [here](https://wiki.servarr.com).

| App        | Description                                                                                           |
|:----------:|:-----------------------------------------------------------------------------------------------------:|
|qBittorrent | Handles downloading your non copyrighted media from places like LegitTorrents or the Internet Archive. |
|Radarr | Movie collection manager |
|Sonarr | Series collection manager |
|Lidarr | Music collection manager |
|Prowlarr | Provides indexing service to the other *arr applications |
|Overseerr | Provides a web interface to request media |
|Requestrr | Provides a Discord bot to request media within channels |
|Unpackerr | Monitors download directories and unzips any compressed media so the managers can import |
|Flaresolver | Solves CloudFlare protection for some indexers that need it |

# Assumptions
* You have a Kubernetes cluster deployed
* You have Helm installed with access to said cluster
* You have an existing PersistentVolumeClaim set up in the namespace you will deploy to that is or links to your media library
* You are okay using hostPath for config directories and download directory (you can mount a network share to this hostPath and skip using the PersistentVolumeClaim for the media library)


## more documentation coming soon...
