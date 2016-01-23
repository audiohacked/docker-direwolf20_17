# Feed-The-Beast Presents Direwolf20 (Minecraft 1.7.10) in a Docker Container
To pull the image:
```
docker pull audiohacked/direwolf20_17:1.9.0
```

It's highly recommended run a data container:
```
docker run --name direwolf20_datastore audiohacked/direwolf20_17:1.9.0 true
```

Then, run the server container:
```
docker run -d --name direwolf20 \
    --volumes-from direwolf20_datastore \
    -p 25565:25565 \
    -e EULA=TRUE \
    audiohacked/direwolf20_17:1.9.0
```
