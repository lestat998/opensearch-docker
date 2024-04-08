# OpenSearch Engine Deployment

This repository contains the necessary Docker configurations to deploy an OpenSearch engine, including OpenSearch Dashboards for visualizations and management. OpenSearch 2.11.0 to take advantage of its open-source features and community-driven enhancements.

## Getting Started

OpenSearch bundles analytical capabilities with search, offering an integrated experience out-of-the-box. This project leverages Docker Compose for the deployment, making it straightforward to get an instance up and running.

### Prerequisites

- Docker and Docker Compose installed on your machine.
- Basic understanding of Docker and containerization.

### Configuration Files

- `docker-compose.yml`: Defines the OpenSearch and OpenSearch Dashboards services, along with their configurations and ports.
- `docker-build.sh`: Script to create the container.
- `docker-delete.sh`: Script to delete the existing container.
- `docker-start.sh`: Script to start the existing container.
- `docker-stop.sh`: Script to stop the existing container.
- `docker-logs.sh`: Script to view the logs of the running container.

### Deployment

To deploy the OpenSearch stack, follow these steps:

1. **Build the Container:**
   Run `./docker-build.sh` to create the Docker container based on the configurations defined in `docker-compose.yml`.

2. **Start the Container:**
   Once the build is complete, you can start the container by running `./docker-start.sh`. This command initializes the OpenSearch and OpenSearch Dashboards services.

3. **Access OpenSearch Dashboards:**
   After the services are up, access OpenSearch Dashboards through `http://localhost:5601` (adjust the port if you've changed the `OPENSEARCH_DASHBOARDS_HOST_PORT` environment variable).

### Additional Commands

- To stop the container, use `./docker-stop.sh`.
- To delete the container, ensuring a clean slate for future deployments, run `./docker-delete.sh`.
- To view the logs of your OpenSearch services for debugging or monitoring, execute `./docker-logs.sh`.

### Docker Compose Highlights

The `docker-compose.yml` file specifies two main services:

- `opensearch`: The core search engine, configured for single-node operation, suitable for development or small-scale environments.
- `opensearch-dashboards`: A web-based user interface for managing, visualizing, and analyzing data stored in OpenSearch.

Both services are set up with basic configurations optimal for getting started quickly. For production environments, further customization and security considerations will be necessary.
