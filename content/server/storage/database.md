---
date: 2000-01-01T00:00:00+00:00
title: Database
author: juliankoehn
weight: 1
aliases:
- /database-settings
- /installation/storage/database/
- /administration/server/database
description: |
  Configure database storage.
---

Music requires the use of a database backend for persistence. Music uses an embedded __sqlite__ database by default, which does not require any additional configuration. This article provides a basic overview of alternate database configurations.

# Postgres

Music supports postgres 9.6 and higher as the database engine. The below example demonstrates postgres database configuration. Please reference the official driver [documentation](https://www.postgresql.org/docs/current/static/libpq-connect.html#LIBPQ-CONNSTRING) for connection string configuration details.

```
MUSIC_DATABASE_DRIVER=postgres
MUSIC_DATABASE_DATASOURCE=postgres://root:password@1.2.3.4:5432/postgres?sslmode=disable
```

# MySQL

Music supports mysql 5.6 and higher as the database engine. The below example demonstrates mysql database configuration. Please reference the official driver [documentation](https://github.com/go-sql-driver/mysql#dsn-data-source-name) for connection string configuration details.

```
MUSIC_DATABASE_DRIVER=mysql
MUSIC_DATABASE_DATASOURCE=root:password@tcp(1.2.3.4:3306)/music?parseTime=true
```