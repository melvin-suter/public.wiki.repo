# OpenSSL Snippets

## Convert PFX to PEM

```bash
openssl pkcs12 -in filename.pfx -nocerts -out key_pw.pem
openssl rsa -in key_pw.pem -out key.pem
openssl pkcs12 -in filename.pfx -clcerts -nokeys -out cert.pem
```

## Create Certificate

```bash
openssl req -new -subj '/CN=localhost.local/O=IT/C=CH'  -newkey rsa:2048 -days 3650 -nodes -x509 -keyout key.pem -out cert.pem
```
