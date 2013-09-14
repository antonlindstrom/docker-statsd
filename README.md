# Docker statsd

This is a simple example of running statsd in docker.

Statsd listens on 8125 by default and is exposed on the as the same on the docker host.

Example to run the docker instance:

    sudo docker run -e GRAPHITE_HOST=graphite.example.com -d statsd

Environment variables that can be used to set options:

    GRAPHITE_PORT (default: 2003)
    GRAPHITE_HOST (default: localhost)
    STATSD_PORT   (default: 8125)
