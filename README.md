# fagdag-juiceshop-ctf

Juice Shop CTF Setup

JuiceShop: [http://localhost:8080/](http://localhost:8080/)
CTFd Score Server: [http://fagdag-ctfd.kefo.no/](http://fagdag-ctfd.kefo.no/)

## Using Docker

### Client Docker compose

```sh
docker-compose up
```

The challenges are now available at http://localhost:8080/

### Client Clean Up

```sh
docker compose rm -v -f
```

## Using Podman

For macOS, you will need `podman` and `podman-compose`.
For Windows, you will need Podman-desktop and `podman-compose`.

### MacOS

[Podman-Desktp MacOs-Install](https://podman-desktop.io/docs/Installation/macos-install)

```sh
brew install podman
brew install podman-compose
#optional
brew install podman-desktop

# Init and Start Podman
podman machine init
podman machine start
podman status

# Run the challange
podman-compose up -d
```

Stopping:

```sh
podman-compose down
```

### Windows

You will need the Podman-Desktop and `podman-compose`
To install, follow the instructions at:

[Podman-Desktop](https://podman-desktop.io/docs/Installation/windows-install)
[Podman-compose](https://github.com/containers/podman-compose#installation)
