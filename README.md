# syncthing_amd64_nanorocks

The service is not centralized as in today's cloud systems, but communication is direct between devices. This service is pre-licensed and is very user-friendly. This service works on the ubuntu / amd64 architecture. There is no need for passwords and usernames are configured.

USAGE:
1)
docker run -v /config --name nanorocks_syncthing_amd64_config amd64/ubuntu chown -R 22000 /config
2)
docker run -d --net='host' -v /mnt/media:/mnt/media --volumes-from nanorocks_syncthing_amd64_config \
-p 22000:22000 -p 8384:8384 -p 21027:21027/udp nanorocks_syncthing_amd64

or Download this shell script for easy usage.
( https://github.com/nanorocks/syncthing_amd64_nanorocks/blob/master/run_syncthing.sh ) 
