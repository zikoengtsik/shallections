# WireGuard Easy

The easiest way to run WireGuard VPN + Web-based Admin UI.

## Overview

### Project Infomation

- **Project Name**: `wg-easy`
- **Root Directory**: `/opt/docker/wg-easy`
- **Container Image**:
  + wg-easy: `ghcr.io/wg-easy/wg-easy:14`

### Directory Structure

```text
/opt/docker/wg-easy
├── data  # Data directory
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
    mkdir -p /opt/docker/wg-easy
    mkdir -p /opt/docker/wg-easy/data
    ```

2. Copy the compose file to `compose.yaml` in the root directory.

    + `compose.with-traefik.yaml`: Deploy the project with Traefik.

3. Copy the `.env.example` file to `.env` in the root directory.
4. Run the command `docker compose -f /opt/docker/wg-easy/compose.yaml up -d` to start the project.
