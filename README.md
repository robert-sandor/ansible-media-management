# Ansible Media Server Playbook

Playbook for deploying a media server using services like Sonarr, Radarr, etc.

WIP - more documentation to be added later

*NOTE*: 

## [qbittorrent](https://github.com/qbittorrent/qBittorrent)

This repo uses the [`linuxserver/qbittorent`](https://docs.linuxserver.io/images/docker-qbittorrent) image by default. This can be changed, but be aware that the settings might not be the same.

You can find the variables for the qbittorrent container under the `qbittorrent` object in the vars file.
By default, this container will start on port `8082`, with the bittorrent port set to `6881`. If you want to change the bittorrent port, make sure to also set the `listen_port` preference.

For qbittorrent preferences, consult the web api for the possible values [qBittorrent Application Preferences](https://github.com/qbittorrent/qBittorrent/wiki/WebUI-API-(qBittorrent-4.1)#get-application-preferences)

[Vuetorrent](https://github.com/WDaan/VueTorrent) will also be downloaded, if the preference to set the alternative web ui is set in the qbittorrent config.