# Gitea

Git with a cup of tea.

## Overview

[Gitea](https://gitea.io/) is a self-hosted Git service. It is designed to be a simple and secure alternative to GitHub, but with a focus on privacy and security.

### Project Infomation

- **Project Name**: `gitea`
- **Root Directory**: `/opt/docker/gitea`
- **Container Image**:
  + gitea: `docker.io/gitea/gitea:1.23.6`
  + postgres: `docker.io/library/postgres:16.8`

### Directory Structure

```text
/opt/docker/gitea
├── data  # Gitea Data directory
├── pgdata  # PostgreSQL Data directory
├── .env  # Environment variables
└── compose.yaml  # Docker Compose file
```

## Getting Started

### Prerequisites

- You have a SMTP server to send emails.
- You add DNS records to your DNS provider correctly.
  + Public DNS Provider: Cloudflare, Google, etc.
  + Private DNS Provider: Host Machine / Router, dnsmasq, etc.

### Installation

1. Create the required directories for the project.

    ```shell
    mkdir -p /opt/docker/gitea
    mkdir -p /opt/docker/gitea/data
    mkdir -p /opt/docker/gitea/pgdata
    ```

2. Copy the compose file to `compose.yaml` in the root directory.

    + `compose.with-traefik.yaml`: Deploy the project with Traefik.

3. Copy the `.env.example` file to `.env` in the root directory, and update the environment variables.
4. Read the "Configuration" section to configure the project.
5. Run the command `docker compose -f /opt/docker/gitea/compose.yaml up -d` to start the project.

## Configuration

### SMTP Configuration

Gitea requires an SMTP server to send emails. Update the relevant environment variables in the `.env` file with your SMTP server details.
