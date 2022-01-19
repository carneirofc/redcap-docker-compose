Generate self-signed cert

```
openssl req \
    -newkey \
    rsa:4096 \
    -nodes \
    -sha256 \
    -keyout certs/key.pem \
    -x509 \
    -days 358000 \
    -out certs/cert.pem
```
