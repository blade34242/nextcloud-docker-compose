# My docker compose file for Nextcloud




````
```
services:
  app:
    image: nextcloud:latest
    restart: always
    network_mode: bridge

    ports:
      - 8080:80
    volumes:
      - /volume3/docker/nextcloudprd/html:/var/www/html
      - /volume3/docker/nextcloudprd/custom_apps:/var/www/html/custom_apps
      - /volume3/docker/nextcloudprd/config:/var/www/html/config
      - /volume3/docker/nextcloudprd/data:/var/www/html/data
      - /volume3/docker/nextcloudprd/themes:/var/www/html/themes/
    environment:
      - PUID=1026
      - PGID=1026
      - TZ=London/Europe
      - MYSQL_DATABASE=<DB>
      - MYSQL_USER=<USER>
      - MYSQL_PASSWORD=<PASSWORD>
```
````
