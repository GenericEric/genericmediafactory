# Generic Media Factory
**Spin up your own media factory in Kubernetes**

These Helm charts are meant to deploy a full-on factory to manage all aspects of your self-hosted media. They utilize the *arr suite of applications for which documentation can be found [here](https://wiki.servarr.com).

| App        | Description                                                                                            |
|:-----------|:-------------------------------------------------------------------------------------------------------|
|[qBittorrent](https://github.com/DyonR/docker-qbittorrentvpn) | Handles downloading your non copyrighted media from places like LegitTorrents or the Internet Archive. VPN enabled in case torrents are not allowed on your network. |
|[SABnzbd](https://github.com/binhex/arch-sabnzbdvpn) | Newsreader for accessing Usenet resources. VPN enabled as well. |
|[Radarr](https://github.com/linuxserver/docker-radarr) | Movie collection manager |
|[Sonarr](https://github.com/linuxserver/docker-sonarr) | Series collection manager |
|[Lidarr](https://github.com/linuxserver/docker-lidarr) | Music collection manager |
|[Readarr](https://github.com/linuxserver/docker-readarr) | Book collection manager |
|[Prowlarr](https://github.com/linuxserver/docker-prowlarr) | Provides indexing service to the other *arr applications |
|[Overseerr](https://github.com/linuxserver/docker-overseerr) | Provides a web interface to request media |
|[Jellyseerr](https://github.com/Fallenbagel/jellyseerr) | Provides a web interface to request media. Integrates with Jellyfin |
|[Requestrr](https://github.com/linuxserver/docker-requestrr) | Provides a Discord bot to request media within channels (This project is no longer supported so use at your own risk) |
|[Unpackerr](https://hotio.dev/containers/unpackerr) | Monitors download directories and unzips any compressed media so the managers can import |
|[Flaresolverr](https://github.com/FlareSolverr/FlareSolverr) | Solves CloudFlare protection for some indexers that need it |

~~~
helm repo add genericmediafactory https://mediafactory.charts.bgeneric.net
helm repo update
helm search repo mediafactory
~~~

# Assumptions
* If you need https access, you have Traefik, Istio, or an external reverse proxy configured.
* You have a Kubernetes cluster deployed (typically a single node [k3s](https://k3s.io/) or [k3d](https://k3d.io/))
* You have Helm installed with access to said cluster
* You have an existing PersistentVolumeClaim set up in the namespace you will deploy to that contains or links to your media library([NFS](https://github.com/kubernetes-sigs/nfs-subdir-external-provisioner), etc)
* You are okay with using hostPath for config directories and download directory (you can mount a network share to this hostPath and skip using the PersistentVolumeClaim for the media library)


## more documentation coming soon...
