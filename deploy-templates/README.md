# database

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.1.0](https://img.shields.io/badge/AppVersion-0.1.0-informational?style=flat-square)

A Helm with database

**Homepage:** <https://github.com/epam/edp-install/>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| KubeRocketCI |  | <https://github.com/epam/edp-install/> |

## Source Code

* <https://github.com/kuberocketci/template-rest-db>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://helm.runix.net | pgadmin4 | 1.57.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| pgadmin4.env.email | string | `"pgadmin@example.com"` |  |
| pgadmin4.extraSecretMounts[0].mountPath | string | `"/pgadmin4/servers.json"` |  |
| pgadmin4.extraSecretMounts[0].name | string | `"servers-config"` |  |
| pgadmin4.extraSecretMounts[0].readOnly | bool | `true` |  |
| pgadmin4.extraSecretMounts[0].secret | string | `"pgadmin-servers-config"` |  |
| pgadmin4.extraSecretMounts[0].subPath | string | `"servers.json"` |  |
| pgadmin4.extraSecretMounts[1].mountPath | string | `"/tmp/pgpassfile"` |  |
| pgadmin4.extraSecretMounts[1].name | string | `"pgpassfile"` |  |
| pgadmin4.extraSecretMounts[1].readOnly | bool | `true` |  |
| pgadmin4.extraSecretMounts[1].secret | string | `"pgadmin-servers-auto"` |  |
| pgadmin4.extraSecretMounts[1].subPath | string | `"pgpassfile"` |  |
| pgadmin4.ingress.enabled | bool | `false` |  |
| pgadmin4.ingress.hosts[0].host | string | `"pgadmin.example.com"` |  |
| pgadmin4.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| pgadmin4.ingress.hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| pgadmin4.persistentVolume.enabled | bool | `true` |  |
| pgadmin4.persistentVolume.size | string | `"1Gi"` |  |
| pgadmin4.serverDefinitions.enabled | bool | `false` |  |
| serverDefinitions.enabled | bool | `true` |  |
| serverDefinitions.maintenanceDB | string | `"postgres"` |  |
| serverDefinitions.resources.limits.cpu | string | `"100m"` |  |
| serverDefinitions.resources.limits.memory | string | `"128Mi"` |  |
| serverDefinitions.resources.requests.cpu | string | `"100m"` |  |
| serverDefinitions.resources.requests.memory | string | `"128Mi"` |  |
| serverDefinitions.secretName | string | `"application-pguser-admin"` |  |
| serverDefinitions.serverGroup | string | `"Servers"` |  |
| serverDefinitions.serverName | string | `"PostgreSQL (pgadmin)"` |  |
| serverDefinitions.sslMode | string | `"prefer"` |  |
