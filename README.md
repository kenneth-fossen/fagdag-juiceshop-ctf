# Fagdag: Let's hack the JuiceShop (CTF)

Nygjerrig på websikkerhet?
I dag er du en hacker, enten aleine eller sammen med en kollega, der vi hacker OWASP Juice Shop. 
Her er det utfordringer for alle, helt fersk eller om du alt henger på the Dark Web. I dag er ikke Juice Shop trygg, når Bouvet hackerteam slår til.

## Beskrivelse


## Juice Shop CTF Setup

JuiceShop: [http://localhost:3000/](http://localhost:3000/)

CTFd Score Server: [http://fagdag-ctfd:8000.kefo.no/](http://fagdag-ctfd:8000.kefo.no/)

## Using Docker

### Install Docker

[Docker Desktop Install (macOS/Windows/Linux)](https://www.docker.com/products/docker-desktop/)
This has both the `docker` and `docker-compose` command.

#### Homebrew install (macOS)

```sh
brew install docker
brew install docker-compose
mkdir -p ~/.docker/cli-plugins
ln -sfn /opt/homebrew/opt/docker-compose/bin/docker-compose ~/.docker/cli-plugins/docker-compose
```

### Client Docker compose

Navigate to the root of the cloned repo.
There should be a `docker-compose.yml` file there, and then you can run the following commands.

```sh
docker-compose up -d 
docker-compose down
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
