# The Restaurant App

This repository contains the project description for the Odilia restaurant voting application.

Odilia is a restaurant voting app based on the Yelb sample application. Users open the frontend in a browser, vote for their favorite restaurant option, and the application updates vote results dynamically.

## Application Components

- `yelb-ui`: frontend used by customers in the browser.
- `yelb-appserver`: API service that receives requests from the frontend.
- `redis-server`: cache/session service.
- `odilia-redis01`: Redis standby service.
- `odilia-redis02`: Redis standby service.
- `odilia-redis-sentinel01`: Redis Sentinel failover service.
- `odilia-redis-sentinel02`: Redis Sentinel failover service.
- `odilia-redis-sentinel03`: Redis Sentinel failover service.
- `yelb-db`: main database service for customer vote data.
- `odilia-db-replication01`: database replication service.
- `odilia-db-replication02`: database replication service.
- `odilia-db-replication03`: database replication service.

## Container Images

The project uses these public images:

- `mreferre/yelb-ui:0.7`
- `mreferre/yelb-appserver:0.5`
- `mreferre/yelb-db:0.5`
- `redis:4.0.2`

## Application Flow

1. A customer opens the frontend application.
2. The frontend sends API requests to the appserver.
3. The appserver reads and writes vote data.
4. Redis supports caching/session behavior.
5. The database stores vote records.
6. The frontend displays updated voting results and page view information.

## Assignment Goal

Deploy the Odilia restaurant application and explain:

- the purpose of each service
- how traffic flows through the app
- how Redis supports the backend
- how the database stores the voting data
- what issues were encountered during deployment
- how those issues were fixed

## Note

This repository intentionally does not include Kubernetes manifest files.

