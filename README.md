# Chrome in Docker optimized for Unraid
Google Chrome is a web browser developed by Google.

RESOLUTION: You can also change the resolution from the WebGUI, to do that simply click on 'Show more settings...' (on a resolution change it can occour that the screen is not filled entirely with the Chrome window, simply restart the container and it will be fullscreen again).

## Env params
| Name | Value | Example |
| --- | --- | --- |
| DATA_DIR | Folder for Chrome | /chrome |
| CUSTOM_RES_W | Enter your preferred screen width | 1280 |
| CUSTOM_RES_H | Enter your preferred screen height | 768 |
| UID | User Identifier | 99 |
| GID | Group Identifier | 100 |
| UMASK | Umask value | 000 |
| DATA_PERM | Data permissions for /chrome folder | 770 |

## Run example
```
docker run --name Chrome -d \
	-p 8080:8080 \
	--env 'CUSTOM_RES_W=1280' \
	--env 'CUSTOM_RES_H=768' \
	--env 'UID=99' \
	--env 'GID=100' \
	--env 'UMASK=000' \
	--env 'DATA_PERM=770' \
	--volume /mnt/cache/appdata/chrome:/chrome \
	ich777/chrome
```
### Webgui address: http://[SERVERIP]:[PORT]/vnc.html?autoconnect=true

This Docker was mainly edited for better use with Unraid, if you don't use Unraid you should definitely try it!

#### Support Thread: https://forums.unraid.net/topic/83786-support-ich777-application-dockers/