### Description
The purpose of this reverse proxy is to solve access problems
with OpenStack installations where the publicURL is not accessible
or the common name in the certificate differs from the advertised
entrypoint.

The proxy directs all traffic to the internalURL and filters endpoint
IPs as well. OpenStack client should be set to the proxy IP instead of
the public or internal URL.

### Configuration
Set both `OS_INTERNAL_IP` and `OS_PUBLIC_IP` environment variables in
`docker-compose.yml` appropriately.

### Prerequisits
* docker
* docker-compose

### Startup
`docker-compose up -d`
