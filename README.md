<h1>GronnFalk Documentation <img src="favicon3.png" alt="GronnFalk Logo" width="40" style="vertical-align: middle;"></h1>

**The simple soap search.**

GronnFalk is an open-source, privacy-focused metasearch engine built for a simple and independent search experience.

[GitHub Repository](https://github.com/LiamProsser77/gronnfalk)

This documentation is open source too. Anyone can edit it and contribute improvements.

[![Docker](https://img.shields.io/badge/Docker-Supported-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)
[![Render](https://img.shields.io/badge/Render-Supported-46E3B7?logo=render&logoColor=black)](https://render.com/)
[![Railway](https://img.shields.io/badge/Railway-Supported-8B5CF6?logo=railway&logoColor=white)](https://railway.com/)
![PHP](https://img.shields.io/badge/PHP-Compatible-777BB4?logo=php&logoColor=white)

---

## Contents

- [About GronnFalk](#about-gronnfalk)
- [Search Sources](#search-sources)
- [GronnFalk Instances](#gronnfalk-instances)
- [Installation](#installation)
- [Linux Installation](#linux-installation)
- [PHP](#php)
- [Docker Installation](#docker-installation)
- [Render](#create-a-render-instance)
- [Railway](#create-a-railway-instance)
- [GitHub Pages](#create-a-github-pages-instance)
- [API](#api)
- [Privacy](#privacy)
- [Contributing](#contributing)
- [Community](#community)
- [License](#license)

---

## About GronnFalk

GronnFalk was founded on August 14, 2026, inspired by a bar of soap whose texture resembled the shape of the project's logo.

GronnFalk is a metasearch engine. It retrieves results from other search sources instead of maintaining its own web index.

GronnFalk is **not a fork of SearXNG**.

The name is inspired by Norwegian-style naming. In English, GronnFalk means Green Falcon.

- **English pronunciation:** GRON-fawk
- **Norwegian pronunciation:** GROON-falk

---

## Search Sources

Search sources associated with GronnFalk include:

- [SearXNG](https://searx-ie07.onrender.com/)
- [4get](https://search.yonderly.org/)
- [DuckDuckGo](https://duckduckgo.com/)
- [Brave Search](https://search.brave.com/)
- [Google](https://google.com/)

Available sources depend on the instance configuration.

---

## GronnFalk Instances

Try one of these GronnFalk instances:

- [GronnFalk on Render](https://gronnfalk-space.onrender.com/index.html)
- [GronnFalk on GitHub Pages](https://liamprosser77.github.io/gronnfalk/)

Find more instances or learn how to create your own on the [GronnFalk Instances website](https://liamprosser77.github.io/gronnfalk-instances/).

---

## Installation

You can deploy GronnFalk using Linux, Docker, Render, or Railway. GitHub Pages can host the static frontend.

[Get the GronnFalk source code](https://github.com/LiamProsser77/gronnfalk)

---

## Linux Installation

### Requirements

- Linux
- Git
- Node.js and npm, if using the Node.js API
- PHP, if running a PHP component

### 1. Install the required software

On Ubuntu or Linux Mint:

```bash
sudo apt update
sudo apt install git nodejs npm php
```

### 2. Download GronnFalk

```bash
git clone https://github.com/LiamProsser77/gronnfalk.git
cd gronnfalk
```

### 3. Install Node.js dependencies

```bash
npm install
```

### 4. Start the API

```bash
npm start
```

This command requires the repository's `package.json` to define a working start script.

### 5. Start a static frontend server

```bash
python3 -m http.server 8080
```

Open [http://localhost:8080](http://localhost:8080).

Configure the frontend to use the correct API URL.

---

## PHP

PHP can serve dynamic web pages and run PHP-based backends. Installing PHP does not automatically convert the existing Node.js API into PHP.

### Run a PHP website locally

If your instance contains an `index.php` file, run:

```bash
php -S localhost:8080
```

Open [http://localhost:8080](http://localhost:8080).

For production, configure a suitable PHP server or Docker image. If your instance still uses the Node.js API, that API must also be running.

---

## Docker Installation

[![Docker](https://img.shields.io/badge/Docker-Supported-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)

Docker lets you package and run an instance in a container.

[Gr onnFalk Docker Repository](https://hub.docker.com/repository/docker/liamprosser77/gronnfalk/general)

### Requirements

- Docker
- Docker Compose, if using a Compose file
- GronnFalk source code

### 1. Download GronnFalk

```bash
git clone https://github.com/LiamProsser77/gronnfalk.git
cd gronnfalk
```

### 2. Build and start the instance

```bash
docker compose up -d --build
```

If the repository includes a suitable Docker Compose file and maps port 8080, open:

[http://localhost:8080](http://localhost:8080)

### 3. Stop the instance

```bash
docker compose down
```

### 4. Update the instance

```bash
git pull
docker compose up -d --build
```

The `Dockerfile` describes how to build the container image. A `docker-compose.yml` file can configure and start the services. The files and required settings must exist for these commands to work.

---

## Create a Render Instance

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/LiamProsser77/gronnfalk)

[![Render](https://img.shields.io/badge/Render-Supported-46E3B7?logo=render&logoColor=black)](https://render.com/)

### Instructions

1. Create an account at [Render](https://render.com/).
2. Connect your GitHub account.
3. Select the GronnFalk repository.
4. Create a new Web Service, or use the deploy link above.
5. Select Docker if you want to build using the repository's `Dockerfile`.
6. Configure environment variables and the service port as needed.
7. Start the deployment.
8. Wait for the build to finish.
9. Open the URL provided by Render.

Make sure the deployment uses a supported runtime and the correct start command. For PHP, configure a compatible PHP runtime or Docker image. For the Node.js API, use the appropriate Node.js command.

Render free services may sleep when idle, depending on the service type and current plan.

---

## Create a Railway Instance

[![Railway](https://img.shields.io/badge/Railway-Supported-8B5CF6?logo=railway&logoColor=white)](https://railway.com/)

[Open Railway](https://railway.com/)

### Instructions

1. Create a Railway account.
2. Create a new project.
3. Choose deployment from a GitHub repository.
4. Select `LiamProsser77/gronnfalk`.
5. Configure the deployment to use the `Dockerfile` if desired.
6. Configure the required environment variables and port.
7. Deploy the service.
8. Open the service's networking settings.
9. Generate a public domain.
10. Visit your new instance.

For PHP, use a compatible PHP runtime or Docker image. For the Node.js API, configure the appropriate start command and settings.

---

## Create a GitHub Pages Instance

GitHub Pages hosts static HTML, CSS, JavaScript, and image files. It does not run PHP or a Node.js backend.

### Instructions

1. Fork the GronnFalk repository.
2. Open the repository's **Settings**.
3. Select **Pages**.
4. Choose deployment from a branch.
5. Select the main branch and the correct folder.
6. Save the settings.
7. Wait for the website to publish.

Typical website address:

```text
https://YOUR-USERNAME.github.io/gronnfalk/
```

Replace `YOUR-USERNAME` with your GitHub username. Configure the frontend to use a working API hosted separately.

---

## API

[GronnFalk API](https://gronnfalk-api-aijg.onrender.com/)

Example search route:

```text
/search?q=dog
```

Check the backend source code for the current routes, response formats, and configuration.

---

## Privacy

- GronnFalk aims to avoid unnecessary tracking.
- The project is open source.
- GronnFalk does not maintain its own web index.
- External search providers may receive queries sent to them.

Self-hosting provides more control, but actual privacy depends on the instance configuration and the providers used.

---

## Contributing

Anyone can help improve GronnFalk by reporting bugs, suggesting features, improving documentation, or submitting code changes.

- [Report an issue](https://github.com/LiamProsser77/gronnfalk/issues)
- [View pull requests](https://github.com/LiamProsser77/gronnfalk/pulls)

---

## Community

[Join the GronnFalk Matrix room](https://app.element.io/#/room/#gronnfalk:matrix.org)

[Visit the GronnFalk Instances website](https://liamprosser77.github.io/gronnfalk-instances/)

---

## License

GronnFalk is licensed under the **Apache License 2.0**.

- [Read the Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0.html)
- [View the GronnFalk license file](https://github.com/LiamProsser77/gronnfalk/blob/main/LICENSE)

This documentation is open source too. You can edit and improve it through GitHub.

---

[GronnFalk](https://liamprosser77.github.io/gronnfalk/) — The simple soap search.
