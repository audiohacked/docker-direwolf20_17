# Feed-The-Beast Presents Direwolf20 (Minecraft 1.7.10) in a Docker Container
It's highly recommended to pull and run a data container:
```
docker pull audiohacked/minecraft_datastore
docker run --name direwolf20_datastore audiohacked/minecraft_datastore
```

Then, pull and run the server container:
```
docker pull audiohacked/direwolf20_17
docker run -d --name direwolf20 \
    --volumes-from direwolf20_datastore \
    -p 25565:25565 \
    -e EULA=TRUE \
    audiohacked/direwolf20_17
```
