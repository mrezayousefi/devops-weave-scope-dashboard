# Docker Network Monitoring with Weave Scope

This project is a simple tool to visualize and inspect network connections between Docker containers. Using **Weave Scope**, you can see a real-time graph of your Docker infrastructure and understand which containers are communicating with each other.

## Setup

The project includes two Docker Compose files:

- `docker-compose-Probe.yml` – sets up the probe container to collect metrics from your Docker environment on all servers.
- `docker-compose-ScopeApp.yml` – launches the Weave Scope application **on the main (prod) server only** to visualize container interactions.

## How to Use

1. On all servers, start the probe:
```bash
docker-compose -f docker-compose-Probe.yml up -d
```

2. start the Scope application:
```bash
docker-compose -f docker-compose-ScopeApp.yml up -d
```

3. Open your browser and access the Weave Scope dashboard to explore the network graph of your containers.
```bash
http://"server svope":4040
```

## Features

- Real-time monitoring of Docker containers
- Interactive network topology visualization
- Helps identify communication patterns between containers
