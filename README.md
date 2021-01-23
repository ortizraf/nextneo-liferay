# Liferay Project
Liferay Portal project configured with MariaDB Database and smtp

## Requirements

- Docker with 8GB RAM available

## Containers

- liferay_portal | port:8080
- mariadb:10.4 | port:3306
- reachfive/fake-smtp-server | port:1080
- elasticsearch | port:9200

## Containers
#### Iniciar aplicação
```nano
docker-compose up
```
#### Parar aplicação
```nano
docker-compose down
```

#### Limpar imagem customizada do Liferay
```nano
docker rmi -f liferay_portal
```

#### Limpar volumes
```nano
docker volume rm liferay_document_library
docker volume rm liferay_mariadb_data
docker volume rm liferay_es01_data
docker volume rm liferay_es02_data
```

#### Exibe uso de máquina
```nano
docker stats
```

CONTAINER ID | NAME | CPU % | MEM USAGE / LIMIT | MEM % | NET I/O | BLOCK I/O | PIDS
--- | --- | --- | --- |--- |--- |--- |---
b64ecb6d3383 | liferay_portal_1 | 2.74% | 4.007GiB / 7.779GiB | 51.51% | 4.11MB / 34.2MB | 525MB / 459MB | 84
85cd47c17b13 | liferay-mariadb | 0.33% | 144.8MiB / 7.779GiB | 1.82% | 1.37MB / 3.1MB | 79.1MB / 2.93MB | 50
c4a6fda9822a | es02 | 1.55% | 830.3MiB / 7.779GiB | 10.42% | 1.77MB / 1.8MB | 18.7MB / 840kB | 51


CONTAINER ID | NAME | CPU % | MEM USAGE / LIMIT | MEM % | NET I/O | BLOCK I/O | PIDS
--- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | ---
b64ecb6d3383 | liferay_portal_1 | 2.74% | 4.007GiB / 7.779GiB | 51.51% | 4.11MB / 34.2MB | 525MB / 459MB | 84
85cd47c17b13 | liferay-mariadb | 0.33% | 144.8MiB / 7.779GiB | 1.82% | 1.37MB / 3.1MB | 79.1MB / 2.93MB | 50
c4a6fda9822a | es02 | 1.55% | 830.3MiB / 7.779GiB | 10.42% | 1.77MB / 1.8MB | 18.7MB / 840kB | 51
efeca32c6a76 | es01 | 1.47% | 825.8MiB / 7.779GiB | 10.37% | 1.88MB / 1.83MB | 8.39MB / 872kB | 48
2a90d35536b5 | liferay_smtp_1 | 0.00% | 25.46MiB / 7.779GiB | 0.32% | 1.36kB / 0B | 0B / 0B | 7