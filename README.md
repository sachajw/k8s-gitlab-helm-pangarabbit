# gitlab-arm64-pangarabbit

A Helm Chart for Gitlab ARM64

![Version: 0.1.22](https://img.shields.io/badge/Version-0.1.22-informational?style=flat-square)
![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)
![AppVersion: 17.0](https://img.shields.io/badge/AppVersion-17.0-informational?style=flat-square)

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Sacha Wharton | <sacha@pangarabbit.com> | <https://github.com/sachajw> |

## Installing the Chart

To install the chart with the release name `gitlab-arm64-pangarabbit`:

```console
$ helm repo add gitlab-arm64-pangarabbit https://sachajw.github.io/gitlab-helm-chart-pangarabbit
$ helm repo update
$ helm install gitlab-arm64-pangarabbit gitlab-arm64-pangarabbit/gitlab-arm64-pangarabbit
```

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://chart.onechart.dev | onechart | 0.69.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| debugSidecarEnabled | bool | `false` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"zengxs/gitlab"` |  |
| image.tag | string | `"17.0"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `"traefik"` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| livenessProbe.httpGet.path | string | `"/"` |  |
| livenessProbe.httpGet.port | string | `"http"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podLabels | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| readinessProbe.httpGet.path | string | `"/"` |  |
| readinessProbe.httpGet.port | string | `"http"` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| secret.enabled | bool | `false` |  |
| securityContext | object | `{}` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.automount | bool | `true` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
| vars | list | `[]` |  |
| volumeMounts | list | `[]` |  |
| volumes[0].name | string | `"gitlab"` |  |
| volumes[0].size | string | `"10Gi"` |  |
| volumes[0].storageClass | string | `"nfs-csi-default"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)