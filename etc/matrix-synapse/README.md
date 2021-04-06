# Matrix configs

## Config

Files:

- [homeserver-wo-federation](https://github.com/shatfel/matrix-template/etc/matrix-synapse/homeserver-wo-federation)
- [homeserver-w-federation](https://github.com/shatfel/matrix-template/etc/matrix-synapse/homeserver-w-federation)

## Variables in configs

| Parameter | Value | Description |
|:----------|:-----:|:------------|
| --regSharedSecret- | hash | generated |
| --email- | email | admin`s email |
| --enableReg- | true/false | allow remote registration |
|--publicKey-|/opt/matrix/public.crt|Public cert|
|--privateKey-|/opt/matrix/private.key|Private key|

## Difference between w and wo

In `homeserver.yaml`.:

```
  - port: 8448
    type: http
    tls: true
    resources:
      - names: [client, federation]
```

And TLS:

```
tls_certificate_path: "/opt/matrix/public.crt"
tls_private_key_path: "/opt/matrix/private.key"
```
> Use letsencrypt or my [Open SSL self-signed](https://github.com/shatfel/openssl-self-signed) generator.