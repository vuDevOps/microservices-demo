See the [documentation](https://microservices-demo.github.io/deployment/docker-compose.html) on how to deploy Sock Shop using Docker Compose.

```zsh
docker-compose up -d
```

```zsh
docker-compose -f docker-compose.monitoring.yml up -d
```

```zsh
docker-compose \
    -f ./deploy/docker-compose/docker-compose.monitoring.yml \
    run \
    --entrypoint /opt/grafana-import-dashboards/import.sh \
    --rm \
    importer
```

Prometheus http://145.108.225.16:9090/

Grafana http://145.108.225.16:3000/login

username: admin, Password: foobar