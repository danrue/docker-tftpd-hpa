# tftpd-hpa Debian Container

Debian-based docker container to run tftpd-hpa.

Git repo: https://github.com/danrue/docker-tftpd-hpa

Docker repo: https://hub.docker.com/r/danrue/tftpd-hpa

## Usage

This container runs tftpd-hpa in the foreground and serves /srv/tftp to port 69
UDP.

Be sure to enable any ports or devices as necessary.

Example usage (docker-compose):

```yaml
    version: '3.4'
    services:
      tftpd-hpa:
        image: danrue/tftpd-hpa
        volumes:
          - tftp:/srv/tftp
        ports:
          - 69:69/udp
    volumes:
      tftp:
        name: tftp-filesystem
```
