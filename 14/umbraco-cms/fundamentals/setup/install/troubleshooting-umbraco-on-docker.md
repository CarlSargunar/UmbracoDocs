---
description: "Since Umbraco 9 it has been possible to run Umbraco CMS natively on Linux or macOS High Sierra 10.13 and newer."
---

# Troubleshooting running Umbraco on Docker

The following are common issues that you may encounter when running Umbraco on Docker.

## Check Images are up to date

The Docker compose example uses Sql Server 2022, but if you have an older version of the image on your machine, a breaking change in the path of sqlcmd may cause the container to fail to start. To fix this, you need to pull the latest image from the Docker Hub.

```bash
docker pull mcr.microsoft.com/mssql/server:2022-latest
```
## Check SQL Server Container is Running


## Check no other services are using the same port

If you have other services running on the same port as the Umbraco service, it will cause a conflict. Most commonly, this happens when you are runing a local instance of SQL Server Express, or another container running SQL Server on the same port.

Check Docker Desktop to see if there are any other containers running on the same port, or if you are on the command line, run the following to see all running containers:

```bash
docker ps
```


## Docker Desktop and Updated

- Check that Docker desktop is running. If it is not running, start it. If it is running, try restarting it.
- Check that Docker Desktop is up to date. If it is not up to date, update it.


