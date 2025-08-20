# Docker Network Monitoring with Weave Scope

This project is a simple tool to visualize and inspect network connections between Docker containers. Using **Weave Scope**, you can see a real-time graph of your Docker infrastructure and understand which containers are communicating with each other.

## Setup

The project includes two Docker Compose files:

- `docker-compose-Probe.yml` – sets up the probe container to collect metrics from your Docker environment.
- `docker-compose-ScopeApp.yml` – launches the Weave Scope application for visualizing container interactions.

## How to Use

1. Start the probe:
```bash
docker-compose -f docker-compose-Probe.yml up -d
```

2. Start the Scope application:
```bash
docker-compose -f docker-compose-ScopeApp.yml up -d
```

3. Open your browser and access the Weave Scope dashboard to explore the network graph of your containers.

## Features

- Real-time monitoring of Docker containers
- Interactive network topology visualization
- Helps identify communication patterns between containers
