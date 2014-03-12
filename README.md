DockerNS
========

DockerNS exposes docker containers as DNS entries based on attributes about the container (such as ID, name).


Configure Docker
----------------

Docker must be configured to use DockerNS as its first DNS server. Ammend your DOCKER_OPTS to include the following before any other `-dns` statement:

    -dns 172.17.42.1

(if your host has another IP address as its bridge, substitue it above).

Currently DockerNS does not offer a recursive DNS service, so to continue using DNS you must pipe DockerNS through a service such as Dnsmasq.


Extras
------

  - Upstart Config - (extra/dockerns.conf)[extra/dockerns.conf]