# Lyrio Dev Container

Dev Container integration for Lyrio platform.

1. This project uses devcontainer to set up the development environment rapidly.
2. Docker-compose is used to set up multiple containers including db, redis, minio, and Lyrio-related containers.
3. The related containers contain 2 submodules: lyrio, lyrio-ui.
4. Dockerfile is used to set up node and nginx environment.

## Setup

1. Clone the repository recursively.
2. Run `cp config-example.yaml config.yaml` and set up smtp server for lyrio backend in config.yaml.
3. Open the project in devcontainer.

## Services

All nginx configuration has the fixed port for every service, and there is no special meaning for them.

- Lyrio-UI: listen 8080
- Lyrio: listen 5050
- MinIO: listen 9090

All services are run on their default port.

- Lyrio-ui: `yarn start` and run on 3000 port.
- Lyrio: `yarn start` and run on 2002 port (defined in config.yaml).

## Running the Services

After entering the container, run `yarn` for both Lyrio-UI and Lyrio, and then execute `yarn start` for both.

```bash
cd lyrio-ui && yarn && yarn start && cd ..
cd lyrio && yarn && yarn start && cd ..
```
