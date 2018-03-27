
# puppetstack

Run a container-based deployment of Puppet Infrastructure.


# Examples

    docker-compose up -d


To scale out more puppet-server

    docker-compose scale puppet=2

To scale down

    docker-compose scale puppet=1


Tada!
