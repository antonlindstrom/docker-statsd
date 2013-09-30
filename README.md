# Docker statsd

This is a simple example of running statsd in docker.

Statsd listens on 8125 by default and is exposed on the as the same on the docker host.

Example to run the docker instance:

    sudo docker run -e GRAPHITE_HOST=graphite.example.com -d antonlindstrom/statsd

Environment variables that can be used to set options:

    GRAPHITE_PORT (default: 2003)
    GRAPHITE_HOST (default: localhost)
    STATSD_PORT   (default: 8125)

This image is available in the docker registry at antonlindstrom/statsd:

    sudo docker pull antonlindstrom/statsd

The [statsd admin interface](https://github.com/etsy/statsd/blob/master/docs/admin_interface.md)
can be accessed through `8126/tcp`. This is not exposed on the host so you'll either
have to know the translated port or the IP of the instance.
