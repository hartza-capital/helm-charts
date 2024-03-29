# ibkr-gateway

![Version: 0.2.8](https://img.shields.io/badge/Version-0.2.8-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 10.19.1m](https://img.shields.io/badge/AppVersion-10.19.1m-informational?style=flat-square)

A Helm chart IBKR Gateway for Kubernetes

**Homepage:** <https://github.com/hartza-capital/helm-charts>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| perriea | <aperrier@hartza.capital> |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity.nodeAffinity.requiredDuringSchedulingIgnoredDuringExecution.nodeSelectorTerms[0].matchExpressions[0].key | string | `"kubernetes.io/arch"` |  |
| affinity.nodeAffinity.requiredDuringSchedulingIgnoredDuringExecution.nodeSelectorTerms[0].matchExpressions[0].operator | string | `"In"` |  |
| affinity.nodeAffinity.requiredDuringSchedulingIgnoredDuringExecution.nodeSelectorTerms[0].matchExpressions[0].values[0] | string | `"amd64"` |  |
| annotations | object | `{}` | annotations is an optional list of annotations to add to the object metadata |
| config | object | `{"credentials":"credentials","live":true,"workers":"workers"}` | config is a list of parameters to pass to the gateway |
| debug | bool | `false` | debug enables debug mode |
| env | list | `[]` | env is a list of environment variables to set in the container. |
| fullnameOverride | string | `""` | fullnameOverride is an optional string to substitute for the full names of resources |
| image | object | `{"pullPolicy":"IfNotPresent","repository":"quay.io/arktos-venture/ibkr-gateway","tag":""}` | Specifies whether a Gateway should be created |
| image.pullPolicy | string | `"IfNotPresent"` | The image pull policy |
| image.repository | string | `"quay.io/arktos-venture/ibkr-gateway"` | The image repository |
| image.tag | string | `""` | The image tag |
| imagePullSecrets | list | `[]` | imagePullSecrets is an optional list of references to secrets in the same namespace to use for pulling any of the images used by this Chart. |
| jvm | object | `{"XX":{"ConcGCThreads":5,"InitiatingHeapOccupancyPercent":70,"MaxGCPauseMillis":200,"ParallelGCThreads":20},"Xms":"2G","Xmx":"2G","installer":{"uuid":"3046c7e3-ffbd-4699-a848-117342ff43ee"}}` | jvm is a list of parameters to pass to the JVM |
| jvm.XX | object | `{"ConcGCThreads":5,"InitiatingHeapOccupancyPercent":70,"MaxGCPauseMillis":200,"ParallelGCThreads":20}` | Xmn is the minimum heap size |
| jvm.Xms | string | `"2G"` | Xms is the initial heap size |
| jvm.Xmx | string | `"2G"` | Xmx is the maximum heap size |
| nameOverride | string | `""` | nameOverride is an optional string to substitute for the full names of resources |
| nodeSelector."kubernetes.io/os" | string | `"linux"` |  |
| podAnnotations | object | `{}` | podAnnotations is an optional list of annotations to add to the pod |
| podSecurityContext | object | `{"fsGroup":10001}` | podSecurityContext is an optional security context to add to the pod |
| resources | object | `{"limits":{"cpu":"300m","memory":"2100Mi"},"requests":{"cpu":"300m","memory":"2100Mi"}}` | resources is an optional list of resources to set for the container |
| securityContext | object | `{"capabilities":{"drop":["ALL"]},"readOnlyRootFilesystem":false,"runAsNonRoot":true,"runAsUser":10001}` | securityContext is an optional security context to add to the container |
| serviceAccount | object | `{"annotations":{},"create":false,"name":""}` | ServiceAccount configuration |
| serviceAccount.annotations | object | `{}` | Annotations to add to the ServiceAccount |
| serviceAccount.create | bool | `false` | Specifies whether a ServiceAccount should be created |
| serviceAccount.name | string | `""` | The name of the ServiceAccount to use. |
| tolerations | list | `[]` |  |
| volumes | object | `{"extra":[],"mounts":[]}` | volumes is a list of volumes that can be mounted |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
