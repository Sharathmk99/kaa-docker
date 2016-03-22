Greetings,

Thanks for checking out this repository. You will find here an easy-to-use Docker image to launch a single-node Kaa server in just a few clicks.
If you don't know about Kaa, check out their home page: http://www.kaaproject.org.

"Kaa is a feature-rich, open-source IoT middleware platform for rapid development of the Internet of Things solutions, IoT applications, and smart products."

## Installation requirements

We suggest you first checkout Kaa's official installation guide before using this image:
-> http://docs.kaaproject.org/display/KAA/Installation+guide

In order to use this image, you will still need to provide the following dependencies:

- PostgreSQL 9.4
- Zookeeper 3.4.5
- MongoDB 2.6.9 OR Cassandra 2.2.5

Note that we have not tested this image with Cassandra; contributions via pull-requests are highly appreciated.

## Quick run

1. Run PostgreSQL, Zookeeper and MongoDB/Cassandra

2. Build this image (build.sh for your convenience)

2. Write up a Docker environment file to configure your server, see example-env.dockerenv. (Don't expose sensitive data in your command line!)

3. Run image, use 'docker-run-kaa-0.8.sh' for convenience (don't forget to edit the env file parameter).

## Logs

If you run your Docker container as a daemon, you won't see its output. That's okay, just run:

$ docker exec <container-name> tail -f /var/log/kaa/kaa-node.log

Or simply run the shortcut script 'view-kaa-node-logs.sh' !


## Notes

This image was originally written to ease deployment and testing. If you find any bugs or misplaced stuff, help us tidy-up with a pull request!


--
Maintainer: Christopher Burroughs
Lead software engineer & architect at xMight Inc., an IoT startup.