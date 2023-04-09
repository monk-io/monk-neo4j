# Neo4j & Monk

This repository contains Monk.io template to deploy Neo4j either locally or on cloud of your choice (AWS, GCP, Azure, Digital Ocean).

## Prerequisites

- [Install Monk](https://docs.monk.io/docs/get-monk)
- [Register and Login Monk](https://docs.monk.io/docs/acc-and-auth)
- [Add Cloud Provider](https://docs.monk.io/docs/cloud-provider)
- [Add Instance](https://docs.monk.io/docs/multi-cloud)

## Make sure monkd is running

```bash
foo@bar:~$ monk status
daemon: ready
auth: logged in
not connected to cluster
```

## Clone Repository

```bash
git clone https://github.com/monk-io/monk-neo4j
```

## Load Template

```bash
cd monk-neo4j
monk load MANIFEST
```

## Let's take a look at the themes I have installed

```bash
foo@bar:~$ monk list neo4j
✔ Got the list
Type      Template  Repository  Version  Tags
runnable  neo4j/db  local       -        -
```

## Deploy Stack

```bash
foo@bar:~$ monk run neo4j/db
```

## Variables

| Variable        | Description                | Default                   |
|-----------------|----------------------------|---------------------------|
| db_port         | Neo4j database port        | 7687                      |
| admin_port      | Neo4j admin interface port | 7474                      |
| image           | Docker image tag           | 5.5                       |
| page_cache_size | Page cache size            | 1G                        |
| heap_size       | Heap size                  | 512M                      |
| max_heap_size   | Max heap size              | 512M                      |

## Stop, remove and clean up workloads and templates

```bash
monk purge -a
```
