## System Design Diagrams
Diagrams are based on the diagrams in the [System Design Primer](https://github.com/donnemartin/system-design-primer/tree/master/solutions/system_design)

### [Mint](https://github.com/donnemartin/system-design-primer/tree/master/solutions/system_design/mint)

```mermaid
---
title: Mint (Simple)
---
graph TB
Client --> web[Web Server] --> accounts[Accounts API]
accounts --> tes[Transaction Extraction Service] --> category[Category Service] & budget[Budget Service] & notif[Notification Service]
accounts --> db
tes --> db[SQL]
tes --> store[Object Store]
```

```mermaid
---
title: Mint (Scaled)
---
graph TB
Client --> DNS & CDN & lb[Load Balancer]
lb --> web[Web Server]
subgraph api
web --> accounts[Accounts API] & read[Read API]
memoryCache[Memory Cache]
end

accounts --> queue[Queue] --> tes


subgraph storage
dbPrimary[(SQL Write Primary)] -.- dbReplica[(SQL Read Replicas)]
objectStore[(Object Store)]
end

subgraph services
tes[Transaction Extraction Service] --> category[Category Service] & budget[Budget Service] & notif[Notification Service]
end

tes --> objectStore
CDN --> objectStore
tes --> dbPrimary
accounts --> dbPrimary & dbReplica
read --> dbReplica & memoryCache[Memory Cache]
```

### [Sales Rank](https://github.com/donnemartin/system-design-primer/tree/master/solutions/system_design/sales_rank)

```mermaid
---
title: Sales Rank (Simple)
---
graph TD
Client --> web[Web Server]
web --> salesApi[Sales API] & readApi[Read API]
service[Sales Rank Service]

subgraph storage
db[SQL]
store[Object Store]
end

service --> db & store
salesApi --> db & store
readApi --> db
```

```mermaid
---
title: Sales Rank (Scaled)
---
graph TD
Client --> DNS & CDN & lb[Load Balancer]
CDN --> store
lb --> web[Web Server] --> salesApi[Sales API] & readApi[Read API]
service[Sales Rank Service]

subgraph storage
dbPrimary[SQL Write Primary] -.- dbReplica[SQL Read Replicas]
store[Object Store]
end

service --> dbPrimary & store
salesApi --> dbPrimary & store
readApi --> dbReplica & store & memoryCache[Memory Cache]

subgraph apis
salesApi
readApi
end

subgraph frontend
Client
DNS
CDN
lb
web
end
```
