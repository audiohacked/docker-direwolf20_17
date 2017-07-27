# Feed-The-Beast Presents Direwolf20 (Minecraft 1.7.10) in a Docker Container
To pull the image:
```
docker pull audiohacked/direwolf20_17:stable
```

It's highly recommended run a named data volume:
```
docker volume create minecraft_direwolf20_data
```

Then, run the server container:
```
docker run --detach --interactive --tty \
    --name direwolf20 \
    --volume minecraft_direwolf20_data:/minecraft/world \
    --publish 25565:25565 \
    --env EULA=TRUE \
    audiohacked/direwolf20_17:stable
```
