[![](https://images.microbadger.com/badges/image/sgtsquiggs/manage-this-node.svg)](https://microbadger.com/images/sgtsquiggs/manage-this-node)

# manage-this-node

This image is derived from [sgtsquiggs/alpine](https://hub.docker.com/r/sgtsquiggs/alpine/).

[Manage-this-node](https://github.com/onedr0p/manage-this-node) is a Node.js port of
[Managethis](https://github.com/Tenzinn3/Managethis), a lightweight portal to view and
manage HTPC webapps.

## Usage
```
docker run \
    --name=manage-this-node \
    -v <path to data>:/config \
    -e PGID=<gid> -e PUID=<uid> \
    -p 3000:3000 \
    sgtsquiggs/manage-this-node
```

## Parameters
* `-p 3000:3000` external port 3000 mapping to internal port 3000
* `-v <path>:/config` where configuation files are stored. Configuration changes require the container to be restarted to take effect.
* `-e PGID=<gid>` for Group ID (see below)
* `-e PUID=<uid>` for User ID (see below)

## User and Group ID
Set these to match the user/group ID of shared data volumes. Files written to these volumes will match the
provided uid/gid.

## Acknowledgements

* [linuxserver/muximux](https://github.com/linuxserver/docker-muximux)
* [chimpchimp/manage-this-node](https://github.com/chimpchimp/docker-manage-this-node)
