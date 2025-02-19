# Neo4j Traefik Example

Execute the following commands to start up Traefik and Neo4j:

```bash
nano .env                   # define your own domain etc.
mkdir certs
echo -n "{}" > acme.json
chmod 600 acme.json
docker compose pull
docker compose up
```

Once Traefik and Neo4j are online, you should be able to open their domains.  
The first visit should fail, as Traefik does not yet have the required TLS certificate from Let's Encrypt. The
certificate should become available within one minute. Problems will be printed to the container's output.
