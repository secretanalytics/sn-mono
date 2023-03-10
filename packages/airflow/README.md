# Secret Network Airflow

We are using docker for local development.

## Running

### Start

```bash
docker-compose up
```

### Add Postgres and Redis services as Airflow connections

- Go to [connections list](http://localhost:8080/connection/list/)
- Add new connection with `postgres` id with the following:
  - Conn Type: `Postgres`
  - Host: `postgres`
  - Schema: `postgres`
  - Login: `postgres`
  - Password: `postgres`
  - Port: `5431`

note: we can prob automate this in the future

### To remove everything

```bash
docker-compose down --volumes --remove-orphans
```

## To use airflow cli

```bash
docker compose run airflow-cli <command>
```

or [install airflow cli wrapper](https://airflow.apache.org/docs/apache-airflow/stable/cli-and-env-variables-ref.html#installing-the-cli)
