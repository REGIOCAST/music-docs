+++
date = "2000-01-01T00:00:00+00:02"
title = "Digital Ocean"
description = "Deploy to the brand new Digital Ocean App Platform"
toc = true
+++

The App Platform gives you the power to quickly and easily build, deploy, manage, and scale apps. It keeps your apps secure by default, i.e., Digital Ocean creates, manages, and renews the SSL certificates while protecting your apps from DDoS attacks.

You can deploy the source code directly from your GitHub repositories (support for GitLab and Bitbucket is coming soon). You can also enable ‘Autodeploy on Push,’ which automatically re-deploys the app each time you push to the branch containing the source code.

The App Platform is one of the few PaaS products built on a shared Kubernetes platform. Digital Ocean automatically analyzes your code, create containers, and run them on Kubernetes clusters. Since Digital Ocean embrace open, cloud-native standards, there’s little to no code customization needed to use the App Platform.

## Project Setup

Create a new App and select the `music` Repository. Set a name, region, and your deployment Branch.

On the next view set your Build Command to:

```
go build github.com/REGIOCAST/music/cmd/music-server
```

The Run Command will be set by DO. You can leave the Port as is, and Run Music with the default Settings on Port 8080. When deploying on DO AppEngine the Domain will have an ACME-Cert provided by DO.

### Environment variables

You should at least set the Storage environment variables. The Digital Ocean Storage `Spaces` is compatible to S3.

```
MUSIC_S3_BUCKET
MUSIC_S3_ACCESS_KEY_ID
MUSIC_S3_SECRET_ACCESS_KEY
MUSIC_S3_REGION
```

### Database

While testing, the built-in SQLite Database is fine. But in a production environment, we recommend using Postgres SQL.

In your Apps Dashboard select `Components` and `+ Create Component`. From the Dropdown select `Database`. Select a name and attach it to your Stack.

```
MUSIC_DATABASE_DATASOURCE=postgres
MUSIC_DATABASE_DATASOURCE=${db.DATABASE_URL}
```

### Healthcheck

In your AppDashboard on the Components, view click on Health Checks => `Edit`. Select `HTTP` and enter `/health` as Path.

That's it. 