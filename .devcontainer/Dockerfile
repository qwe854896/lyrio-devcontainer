FROM mcr.microsoft.com/vscode/devcontainers/javascript-node:16

WORKDIR /workspace

# Install nginx
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends nginx \
    && apt-get clean -y && rm -rf /var/lib/apt/lists/*

CMD ["nginx", "-g", "daemon off;"]
