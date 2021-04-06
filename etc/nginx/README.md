# nginx config

## Config

Files:
- [matrix-w-federation.conf](https://github.com/shatfel/matrix-template/etc/nginx/matrix-w-federation.conf)
- [matrix-wo-federation.conf](https://github.com/shatfel/matrix-template/etc/nginx/matrix-wo-federation.conf)

## Variables in configs

| Parameter | Value | Description |
|:----------|:-----:|:------------|
|--serverName-|dns resolved host name|host name|
|--sslPort-|8443 or 443|Port where matrix listen SSL|
|--publicKey-|/opt/matrix/public.crt|Public cert|
|--privateKey-|/opt/matrix/private.key|Private key|

> Use letsencrypt or my [Open SSL self-signed](https://github.com/shatfel/openssl-self-signed) generator.