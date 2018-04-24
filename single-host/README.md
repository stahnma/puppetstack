# Create a Single Puppet Host with Docker Compose

1. Create an external volume for the postgres database

``` bash
> docker volume create --name puppetdb-postgres-volume -d local
```

2. Start the composition

``` bash
> docker-compose up
```

3. Wait for a while ...

The initialization process can take a while and may appear to throw errors.  Just wait awhile and eventually all of the components just sort themselves out

4. Put your Puppet code etc. into the `code` directory, as you would with R10K or Puppet Code Manager


# Destroy a Single Puppet Host with Docker Compose

1. Stop docker-compose with Ctrl-C

2. Remove the resources with docker-compose

``` bash
> docker-compose down
```

3. Remove the volume

``` bash
> docker volume rm puppetdb-postgres-volume
```
