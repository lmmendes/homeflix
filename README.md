# Homeflix

A repository that setups' transmission, jackett, sonarr, radarr, overseerr and plex for local viewing.

## Installing

### Environment file .env

We need to create a file named `.env` to handle the configuration were the media is going to be stored and the file permissions, here are the available configuration:

| VARIABLE           | TYPE    | Description                                            |
|--------------------|---------|--------------------------------------------------------|
| PUID               | integer | User ID                                                |
| PGID               | integer | Group ID                                               |
| STORAGE_FOLDER     | String  | Local folder were the media files will be stored.      |
| APPS_CONFIG_FOLDER | String  | Local folder were the apps config files will be stored |
| PLEX_CLAIM         | String  | Plex Claim Code, https://www.plex.tv/claim/            |

#### Configuration `PUID` and `PGID`

```bash
> id $user
uid=501(mike) gid=20(staff) groups=20(staff),12(everyone)...
```


Here we can see that `id $user` returned `uid=501(mike)` and `gid=20(staff) groups=20(staff)...`

For the `PUID` use the number `501` from the `uid=501(mike)` and for `PGID` use any of the numbers from `gid=20(staff)` or `groups=20(staff)` for this let's use `20`.

This means the content on the `.env` file should look a bit like this:

```bash
PUID=501
PGID=20
```

#### Configuration `STORAGE_FOLDER`

#### Configuration `APPS_CONFIG_FOLDER`

##### Configuration `PLEX_CLAIM`


## App urls

| App          | URL                      | Description                                                                                                                                      |
|--------------|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Jackett      | http://jackett:9117      | Jackett works as a proxy server: it translates queries from apps (Sonarr, Radarr, SickRage, CouchPotato, Mylar, etc) into tracker-site-specific  |
| Transmission | http://transmission:9091 | Transmission is a BitTorrent client                                                                                                              |
| Plex         | http://plex:32400/web    | Plex is a streaming media service                                                                                                                |
| Sonarr       | http://sonarr:8989       | Sonarr find tv show releases and sends them directly to your download client                                                                     |
| Radarr       | http://radarr:7878       | Sonarr find movie releases and sends them directly to your download client                                                                       |
| overseerr    | http://overseerr:5055    | Overseerr is a request management and media discovery tool built to work with Plex, Sonarr and Radarr                                            |
