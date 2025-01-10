# Enigma TUI web
Enigma TUI web is a project to host all the artifacts needed to expose Enigma TUI via web using container technology.

Relevant commands:

```console
$ export DOCKER_USERNAME=<username>
$ podman build --build-arg TARGETPLATFORM=linux/amd64 --build-arg PUBLICURL=http://localhost:8000 -t docker.io/$DOCKER_USERNAME/enigma-tui-web:v2_enigmatui-1.0.2 ./src
$ podman run -ti --rm -p 8000:8000 docker.io/$DOCKER_USERNAME/enigma-tui-web:v2_enigmatui-1.0.2
$ podman login docker.io --username $DOCKER_USERNAME
$ podman push docker.io/$DOCKER_USERNAME/enigma-tui-web:v2_enigmatui-1.0.2
```