# Homeflix

A repository that setups' transmission, jackett, sonarr, radarr, overseerr and plex for local viewing.

## Installing

1. Create `.env` file

| VARIABLE           | TYPE    | Description                                            |
|--------------------|---------|--------------------------------------------------------|
| PUID               | integer | User ID                                                |
| PGID               | integer | Group ID                                               |
| STORAGE_FOLDER     | String  | Local folder were the media files will be stored.      |
| APPS_CONFIG_FOLDER | String  | Local folder were the apps config files will be stored |
| PLEX_CLAIM         | String  | Plex Claim Code, https://www.plex.tv/claim/            |


> id $user

## App urls

| App          | URL                      | Description                                                                                                                                      |
|--------------|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Jackett      | http://jackett:9117      | Jackett works as a proxy server: it translates queries from apps (Sonarr, Radarr, SickRage, CouchPotato, Mylar, etc) into tracker-site-specific  |
| Transmission | http://transmission:9091 | Transmission is a BitTorrent client                                                                                                              |
| Plex         | http://plex:32400/web    | Plex is a streaming media service                                                                                                                |
| Sonarr       | http://sonarr:8989       | Sonarr find tv show releases and sends them directly to your download client                                                                     |
| Radarr       | http://radarr:7878       | Sonarr find movie releases and sends them directly to your download client                                                                       |
| overseerr    | http://overseerr:5055    | Overseerr is a request management and media discovery tool built to work with Plex, Sonarr and Radarr                                            |
