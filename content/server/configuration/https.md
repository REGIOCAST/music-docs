---
date: 2000-01-01T00:00:00+00:00
title: Certificates
author: juliankoehn
weight: 20
separator: true
aliases:
- /installation/security/ssl/
- /installation/security/ssl-lets-encrypt/
- /configure-ssl/
- /configure-lets-encrypt/
- /administration/server/ssl
- /administration/server/ssl-with-lets-encrypt
description: |
  Configure server security.
---

# Lets Encrypt

Music supports automated SSL configuration and updates using Let's Encrypt. You can enable Let’s encrypt with the following flag:

1. Enable Lets Encrypt with the following parameter:
    ```
    MUSIC_TLS_AUTOCERT=true
    ```

2. Ensure the desired hostname is configured:

    ```
    MUSIC_SERVER_HOST=domain.com
    MUSIC_SERVER_PROTO=https
    ```

3. Expose the standard http and https ports:

    ```
    docker run \
    -p 80:80 \
    -p 443:443
    ```

4. Mount the certificate cache to the host:

    ```
    docker run \
    -v /var/lib/music:/data
    ```

## Certificate Cache

Music caches generated certificates on disk at `/data/golang-autocert`. This prevents the system from re-requesting certificates on restart. It is best practice to bind mount the `/data` directory to the host.

## Certificate Upgrades

Music uses the official Go acme library which will handle certificate upgrades. There should be no additional configuration or management required.