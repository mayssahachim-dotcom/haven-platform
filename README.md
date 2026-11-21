# haven-platform

Managing Docker clusters often means switching between tools for nodes, containers, images, registries, and scheduled work. haven-platform brings these tasks into one web-based platform built around Docker, Swarm, and Compose.

**Use the dashboard to inspect cluster state and manage Docker resources from one place.**

## Features

- Monitor cluster, node, and container status from a dashboard.
- Manage Swarm clusters, including nodes, containers, and cluster event logs.
- Inspect containers, view logs, and review container configuration.
- Manage images across clusters and remove images that are no longer needed.
- Configure public or private registries and schedule unattended jobs.
- Delegate administrative access to specific clusters.

## Installation

haven-platform is a Java application. Install a compatible JDK and Maven, then build the project from source:

```bash
git clone https://github.com/codeabovelab/haven-platform.git
cd haven-platform
java -version
mvn clean package
```

The build places its artifacts in `target/`. Start the generated application JAR with a port setting such as:

```bash
java -jar target/<built-application>.jar --server.port=8080
```

Configure access to the Docker and Swarm environments through the application properties described in the project documentation. The managed Docker hosts and registries must be reachable by the running application.

See [`doc/installation.md`](doc/installation.md) and [`doc/`](doc/) for project-specific installation and configuration details.

## Usage

Start the application, then open the web interface at `http://localhost:8080`:

```bash
java -jar target/<built-application>.jar --server.port=8080
```

Use the dashboard to review cluster health. From the management modules, inspect nodes and containers, review logs, manage images, configure registries, schedule jobs, and assign cluster-level administrative access.

## License

haven-platform is licensed under the Apache License, Version 2.0 (Apache-2.0).

This project is based on [`codeabovelab/haven-platform`](https://github.com/codeabovelab/haven-platform). Copyright 2017 Code Above Lab Inc. See [`LICENSE`](LICENSE) for the complete license text and attribution terms.
