In order to use REDcap valid ssl certificates are required.

Place the certificate and the private key into the `SSL_CERT_DIR`.

```
SSL_CERT_FILE=/usr/local/apache2/conf/certs/cert.pem
SSL_KEY_FILE=/usr/local/apache2/conf/certs/key.pem
SSL_CERT_DIR=../certs
```

For testing purposes, one can generate self-signed certificates.
Be warned that the system will not behave as expected using self-signed.

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
