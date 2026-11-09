# Home Assistant package for Elastic

> [!WARNING]
> **This repository is archived and no longer maintained.**
>
> To send Home Assistant logs to Elasticsearch, use the
> [Elastic Agent app for Home Assistant](https://github.com/legrego/homeassistant-elastic-agent-app)
> instead. It reads the systemd journal, so it collects Home Assistant Core,
> Supervisor, app and host logs, and it parses Core log lines (including
> tracebacks) into ECS fields.
>
> This package reads `/config/home-assistant.log`, which Home Assistant OS no
> longer writes by default. It also targets older versions of the Elastic Stack
> and the package spec (`format_version` 2.8.0, Kibana 8.9, the deprecated
> `logfile` input).
>
> For entity state changes, see the
> [Elasticsearch integration for Home Assistant](https://github.com/legrego/homeassistant-elasticsearch).

This is an integration package for the Elastic Stack.

## Dependecies

To build this package, you need [elastic-package](https://github.com/elastic/elastic-package). More details on how to work with integrations can be found [here](https://github.com/elastic/integrations).

## Build and run

* Setup the elastic stack: `elastic-package stack up -v`
* Install package: `elastic-package install`
* Open: https://localhost:5601/app/home#/
  * Username: elastic
  * Password: changeme
