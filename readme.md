Home Media Center Setup

This repository contains a docker-compose.yml file for setting up a complete
home media center. It includes services for torrent downloading, media
organization, and streaming, all containerized using Docker. 

Services Included

- qBittorrent: A BitTorrent client for downloading media. http://home:8082
- Jackett: A proxy server for torrent indexers, helping you find torrents.
  http://home:9117
- Radarr: A movie collection manager that automatically finds and downloads
  movies using torrents.  http://home:7878
- Metube: A YouTube video downloader service. http://home:8081
- Jellyfin: A media server for organizing and streaming your media.
http://home:8096 
- Flaresolverr: A service for bypassing anti-bot. http://home:8191

Setup

1. Just hit `docker compose up -d` to get everything up.
2. In Jackett, you need to create at least 1 indexer.
3. In Radarr, you need to add root folder (/downloads), downloader as the qb, 
    and the indexer from jackett.
4. After that, the only thing you need to do is searching and adding movie in 
    radarr and watch it in jellyfin later.
