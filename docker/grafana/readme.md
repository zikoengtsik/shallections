# Grafana

Grafana is a platform for visualizing metrics, logs, and traces from multiple sources.

## Overview

[Grafana](https://grafana.com/) is a platform for visualizing metrics, logs, and traces from multiple sources.
Grafana OSS provides you with tools to display that data on live dashboards with insightful graphs and visualizations.

### Project Information

- **Project Name**: `grafana`
- **Root Directory**: `/opt/docker/grafana`
- **Container Image**:
  + grafana: `docker.io/grafana/grafana-oss:11.6.0`
  + postgres: `docker.io/library/postgres:16.8`

### Directory Structure

```text
/opt/docker/grafana
├── data  # Grafana Data directory
├── pgdata  # PostgreSQL Data directory
├── .env  # Environment variables
└── compose.yaml  # Docker Compose file
```

## Getting Started

### Prerequisites

- You add DNS records to your DNS provider correctly.
  + Public DNS Provider: Cloudflare, Google, etc.
  + Private DNS Provider: Host Machine / Router, dnsmasq, etc.

### Installation

1. Create the required directories for the project.

    ```shell
    mkdir -p /opt/docker/grafana
    mkdir -p /opt/docker/grafana/data
    mkdir -p /opt/docker/grafana/pgdata
    ```

2. Copy the compose file to `compose.yaml` in the root directory.

    + `compose.with-traefik.yaml`: Deploy the project with Traefik.

3. Copy the `.env.example` file to `.env` in the root directory, and update the environment variables.
4. Read the "Configuration" section to configure the project.
5. Run the command `docker compose -f /opt/docker/grafana/compose.yaml up -d` to start the project.

## Configuration

None
