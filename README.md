# Docker PostgreSQL 11.4
Why postgresql 11.4 ? TimescaleDB is available only for this version of postgreSQL
So I built this docker image to get that time-serie feature. 

## Build and Run 
```shell script
    https://github.com/system-dev-formations/docker-postgres11.4.git
    cd docker-postgres11.4 
    groupadd -g 70 postgres
    adduser -g 70 -u 70 postgres
    docker build -t postgres:11.4 .
    mount -t glusterfs gluster01:/gv0 /mnt
    docker run -d --name db --rm -p 15432:5432 -v /mnt:/var/lib/postgresql/data postgres:11.4  

```
