# SSL certificates dir

Default directory to be mounted into the apache container `rdc/docker-web`.

**REDCAP WILL ONLY WORK AS EXPECTED WITH VALID SIGNED CERTIFICATES**

For testing purposesn the self self-signed certificate can be generated using the following command:
```
openssl req \
    -newkey \
    rsa:4096 \
    -nodes \
    -sha256 \
    -keyout pem.key \
    -x509 \
    -days 358000 \
    -out pem.crt
```
