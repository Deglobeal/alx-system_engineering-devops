# www.foobar.com Scaled-Up Infrastructure

## Overview

This infrastructure hosts the www.foobar.com website using a scalable, fault-tolerant design separating web, application, and database components on dedicated servers. Two HAProxy load balancers are clustered for high availability.

## Components

- **Load Balancers (2x HAProxy):** Distribute incoming requests evenly and provide failover capability.
- **Web Servers (2x Nginx):** Serve static content and reverse proxy dynamic requests.
- **Application Servers (2x):** Run backend business logic and communicate with the database.
- **Database Server:** MySQL Primary-Replica cluster managing persistent data storage.

## Benefits

- High availability at load balancer level prevents SPOF.
- Dedicated servers for each component allow independent scaling and security.
- Clustering load balancers ensures continuous service during failures.
- Clear separation of responsibilities simplifies maintenance and upgrades.

## How to Scale Further

- Add more web or app servers behind load balancers.
- Implement multi-master or sharded database clusters for write scaling.
- Use monitoring tools to track performance and detect bottlenecks.

