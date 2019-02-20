# docker-postgis

* Based on [kartoza/postgis](https://registry.hub.docker.com/u/kartoza/postgis/)

* Added some extensions to PostGIS (Edited **setup-database.sh**)

```bash
-- sfcgal not available with all distributions
CREATE EXTENSION postgis_sfcgal;
-- fuzzy matching needed for Tiger
CREATE EXTENSION fuzzystrmatch;
-- rule based standardizer
CREATE EXTENSION address_standardizer;
-- example rule data set
CREATE EXTENSION address_standardizer_data_us;
-- Enable US Tiger Geocoder
CREATE EXTENSION postgis_tiger_geocoder;
```

# Installation

* Clone this repository

* Build a docker image

```bash
docker build -t my_postgis .
```
