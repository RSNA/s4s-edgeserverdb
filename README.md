# s4s-edgeserverdb
Postgres database to support RSNA Edge Server in S4S project

This docker image provides Postgresql initialization for the RSNA Edge Server
test database used to test FHIR DiagnosticReport queries for Radiology Reports.
It extends the [official postgres image](https://hub.docker.com/_/postgres/).

# How to use this image

## start a postgres instance

```
docker run --name rsnadb \
   -p 5433:5432 \
   -v /etc/localtime:/etc/localtime \
   -e POSTGRES_DB=rsnadb \
   -e POSTGRES_USER=edge \
   -e POSTGRES_PASSWORD=psword \
   -d rsna/s4s-edgeserverdb
````
