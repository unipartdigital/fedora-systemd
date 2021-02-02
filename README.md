Fedora systemd single-command container
=======================================

[![Build](https://img.shields.io/github/workflow/status/mcb30/fedora-systemd/Build)](https://github.com/mcb30/fedora-systemd/actions?query=workflow%3ABuild+branch%3Amaster)

This container provides a Fedora environment in which to execute an
arbitary specified command with all enabled ``systemd`` services
running in the background.  For example:

    podman run -i -t mcb30/fedora-systemd /bin/sh

The container will shut down cleanly once the specified command exits,
and the final exit status of the container will reflect the exit
status from the specified command.

If no command is specified, then the container will simply run all
enabled ``systemd`` services.

The container is published on Docker Hub as
[`mcb30/fedora-systemd`](https://hub.docker.com/r/mcb30/fedora-systemd/).
