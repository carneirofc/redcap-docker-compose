# SSL certificates dir

Default directory to be mounted into the apache container `rdc/docker-web`.

Generating the certificate:

```bash
openssl pkcs12 -in <domain>.pfx -out <domain>.crt -nokeys -clcerts

openssl pkcs12 -in <domain>.pfx -out <domain>.key -nocerts -nodes
```

## self-signed **REDCAP WILL ONLY WORK AS EXPECTED WITH VALID SIGNED CERTIFICATES**

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
