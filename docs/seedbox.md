# Seedbox

## filebrowser - file browser webapp

### Installing
1. `docker pull filebrowser/filebrowser`
2. create empty `filebrowser.db` file
```
touch filebrowser.db
```

Running
```
docker run \
    -v /path/to/root:/srv \
    -v /path/to/filebrowser.db:/database/filebrowser.db \
    -v /path/to/settings.json:/config/settings.json \
    -e PUID=$(id -u) \
    -e PGID=$(id -g) \
    -p 8080:80 \
    filebrowser/filebrowser:s6
```

## mango - manga reader webapp

### Installing
1. `docker pull hkalexling/mango`
2. create `docker-compose.yml` (see https://hub.docker.com/r/hkalexling/mango)

### Running
3. `docker-compose up`

whatbox will probably prevent you from opening certain ports and will suggest another port, edit `docker-compose.yml` to use the suggested port.

