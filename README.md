# Tags

* **rancher_files**: copy over the following files: 
  * rc.local
  * root vimrc
  * usb_reset.c

* **rancher_install**: same as with rancher_files but also install software such as gcc,
screen, mhddfs and so on. Will also compile usb_reset and create the docker
volumes required by the *services* tag

* **rancher_docker_setup**: creates and fill docker_volumes required by services.
  Creates required docker networks as well

* **rancher_services**: start all defined containers

==VPN enabled services==

All the services that are vpn enabled need to have their ovpn files provided.
Said files are generated properly by the vpn role (**gencert** tag). if you want
to use your own, here is the naming scheme:

*vpn.url_service_name.ovpn*
