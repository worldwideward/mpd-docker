# MPD in docke

how to use this image
```bash
docker run --name mpd -p 8000:8000 -p 6600:6000 -v $HOME/Music:/var/lib/mpd/music -d cr.oblak.be/experiments/mpd
```
The audio stream will be available at http://localhost:8000, the controls (using mpc/ncmpcpp/...) at localhost:6600
You can exec into the running container to add music:
```bash
docker exec -it mpd bash
addSong <url>
```
Songs will automatically be downloaded to your music directory, but don't forget to update your mpd's database to be able to add it to the playlist.
Enjoy!
