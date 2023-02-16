# Fagdag: Let's hack the JuiceShop (CTF)

Nygjerrig på websikkerhet?
I dag er du en hacker, enten aleine eller sammen med en kollega, der vi hacker OWASP Juice Shop.
Her er det utfordringer for alle, helt fersk eller om du alt henger på the Dark Web. I dag er ikke Juice Shop trygg, når Bouvet hackerteam slår til.

## Kort oversikt

Vi samler oss og tar en liten gjennomgang felles.

- Hva er JuiceShop?
- Hva er en CTF?
- Hvorfor (learning goals)
- Tools

## Let's get going!

Alle må lage konto på vår private [CTFd](http://fagdag-ctfd.kefo.no/), her kan de som har lyst samle seg i Team og jobbe sammen lage et team og joine det.
Om du har lyst å jobbe aleine, så er det helt fint, bare lagt et team med bare deg i.
Challenges og Scoreboard åpner kl 1230 og vi holder på så lenge vi har det gøy.

PS: Du trenger ikke bruke ekte navn eller e-post. Finn ditt hacker nick ;)

## Planen

| Kl | |  
| --- | --- |
| 1200 | Oppmøte Skostredet & Intro |
| 1220 | Pause  |
| 1230 | JuciceShop med CTFd (m/pauser når det passer) |
| 1600 | Helg |

## Juice Shop CTF Setup

JuiceShop: [http://localhost:3000/](http://localhost:3000/)

CTFd Score Server: [http://fagdag-ctfd.kefo.no/](http://fagdag-ctfd.kefo.no/)

Backup: [http://fagdag-ctfd.kefo.no:3000](http://fagdag-ctfd.kefo.no:3000)

## Getting ready

Du trenger enten Docker eller Podman.
Podman er gratis, og Docker må du ha lisens om du begynner å bruke det når du utvikler.

## Using Docker

### Install Docker


#### Homebrew install (macOS)

```sh
brew install docker
brew install docker-compose
mkdir -p ~/.docker/cli-plugins
ln -sfn /opt/homebrew/opt/docker-compose/bin/docker-compose ~/.docker/cli-plugins/docker-compose
```

### Windows Install

[Docker Desktop Install (macOS/Windows/Linux)](https://www.docker.com/products/docker-desktop/)
This has both the `docker` and `docker-compose` command.

### Docker Compose (client)

Navigate to the root of the cloned repo.
There should be a `docker-compose.yml` file there, and then you can run the following commands.

```sh
docker-compose up -d 
docker-compose down
```

The challenges are now available at [http://localhost:3000/](http://localhost:3000/)

### Docker Compose (client clean-up)

To clean up and remove the docker container, you can from the same root folder, run:
```sh
docker compose rm -v -f
```

## Using Podman

### Install PodMan

For macOS, you will need `podman` and `podman-compose`.
For Windows, you will need Podman-desktop and `podman-compose`.

#### MacOS

[Podman-Desktp MacOs-Install](https://podman-desktop.io/docs/Installation/macos-install)

```sh
brew install podman
brew install podman-compose
#optional (but it is very nice)
brew install podman-desktop

# Init and Start Podman
podman machine init
podman machine start
podman status
```

#### Windows

You will need the Podman-Desktop and `podman-compose`
To install, follow the instructions below.

##### Podman Desktop

[Podman-Desktop](https://podman-desktop.io/docs/Installation/windows-install)

#### Podman-compose

[Podman-compose](https://github.com/containers/podman-compose#installation)

TL;DR:
Install the latest stable version from PyPI:

```sh
pip3 install podman-compose
```

pass `--user` to install inside regular user home without being root.

### Podman-Compose (client)

Starting and stopping:

```sh

podman-compose up -d
# Stopping
podman-compose down
```




### Podman-Compose (client)

Navigate to the root of the cloned repo.
There should be a `docker-compose.yml` file there, and then you can run the following commands.

```sh
# Start the challange
podman-compose up -d 
# Stopping
podman-compose down
```

The challenges are now available at [http://localhost:3000/](http://localhost:3000/)

### Podman-Compose (client clean-up)

```sh
podman-compose rm -v -f
```