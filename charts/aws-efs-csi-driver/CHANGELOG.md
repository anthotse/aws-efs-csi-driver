# Helm chart
# v3.2.1
* Bump app/driver version to `v2.1.10`
# v3.2.0
* Bump app/driver version to `v2.1.9`
# v3.1.9
* Bump app/driver version to `v2.1.8`
# v3.1.8
* Bump app/driver version to `v2.1.7`
# v3.1.7
* Bump app/driver version to `v2.1.6`
# v3.1.6
* Bump app/driver version to `v2.1.5`
# v3.1.5
* Bump app/driver version to `v2.1.4`
# v3.1.4
* Bump app/driver version to `v2.1.3`
# v3.1.3
* Bump app/driver version to `v2.1.2`
# v3.1.2
* Bump app/driver version to `v2.1.1`
# v3.1.1
* Bump app/driver version to `v2.1.0`
# v3.1.0
* Bump app/driver version to `v2.0.9`
# v3.0.9
* Bump app/driver version to `v2.0.8`
# v3.0.8
* Bump app/driver version to `v2.0.7`
# v3.0.7
* Bump app/driver version to `v2.0.6`
# v3.0.6
* Bump app/driver version to `v2.0.5`
# v3.0.5
* Bump app/driver version to `v2.0.4`
# v3.0.4
* Bump app/driver version to `v2.0.3`
# v3.0.3
* Bump app/driver version to `v2.0.2`
# v3.0.2
* Update Helm to use the image from Public ECR rather than DockerHub
# v3.0.1
* Bump app/driver version to `v2.0.1`
# v3.0.0
* Bump app/driver version to `v2.0.0`
# v2.5.7
* Bump app/driver version to `v1.7.7`
# v2.5.6
* Bump app/driver version to `v1.7.6`
# v2.5.5
* Bump app/driver version to `v1.7.5`
# v2.5.4
* Bump app/driver version to `v1.7.4`
# v2.5.3
* Bump app/driver version to `v1.7.3`
# v2.5.2
* Bump app/driver version to `v1.7.2`
# v2.5.1
* Bump app/driver version to `v1.7.1`
# v2.5.0
* Bump app/driver version to `v1.7.0`
# v2.4.9
* Bump app/driver version to `v1.6.0`
# v2.4.8
* Bump app/driver version to `v1.5.9`
# v2.4.7
* Bump app/driver version to `v1.5.8`
# v2.4.6
* Bump app/driver version to `v1.5.7`
# v2.4.5
* Bump helm version for change of state-dir path to avoid losing track of state files which exists already to `v2.4.5`
# v2.4.4
* Bump helm version to pick the latest side-car images `v2.4.4`
# v2.4.3
* Bump app/driver version to `v1.5.6`
# v2.4.2
* Bump app/driver version to `v1.5.5` 
# v2.4.1
* Bump app/driver version to `v1.5.4`
# v2.4.0
* Bump app/driver version to `v1.5.3`
# v2.3.9
* Bump app/driver version to `v1.5.2`
# v2.3.8
* Bump app/driver version to `v1.5.1`
# v2.3.7
* Bump app/driver version to `v1.5.0`
# v2.3.6
* Bump app/driver version to `v1.4.9`
# v2.3.5
* Bump app/driver version to `v1.4.8`

# v2.3.4
* Bump app/driver version to `v1.4.7`

# v2.3.3
* Bump app/driver version to `v1.4.6`

# v2.3.2
* Bump app/driver version to `v1.4.5`

# v2.3.1
* Bump app/driver version to `v1.4.4`

# v2.3.0
* Bump app/driver version to `v1.4.3`

# v2.2.9
* Bump app/driver version to `v1.4.2`

# v2.2.8
* Bump app/driver version to `v1.4.1`

# v2.2.7
* Bump app/driver version to `v1.4.0`
# v2.2.6
* Bump app/driver version to `v1.3.8`

# v2.2.5
* Bump app/driver version to `v1.3.7`

# v2.2.4
* Add STS regional endpoints flag to fix PV creation on private EKS

# v2.2.3
* Bump app/driver version to `v1.3.6`

# v2.2.2
* Add controller.volMetricsOptIn for emitting volume metrics
* Update ECR sidecars to 1-18-13

# v2.2.1
* Bump app/driver version to `v1.3.5`

# v2.2.0
* Allow health ports to be configured
* Add Missing "patch" permission for "events"

# v2.1.6
* Bump app/driver version to `v1.3.4`

# v2.1.5
* Bump app/driver version to `v1.3.3`

# v2.1.4
* Add node.serviceAccount values for creating and/or specifying daemonset service account

# v2.1.3
* Bump app/driver version to `v1.3.2` 

# v2.1.2
* Add extra-create-metadata

# v2.1.1
* Update app/driver version to `v1.3.1`

# v2.1.0

## New features
* Update app/driver version to `v1.3.0`

## Bug fixes
* Put comments back in place inside the values file ([#475](https://github.com/kubernetes-sigs/aws-efs-csi-driver/pull/475), [@pierluigilenoci](https://github.com/pierluigilenoci))

# v2.0.1

## Bug fixes
* Helm chart: fix reclaimPolicy and volumeBindingMode ([#464](https://github.com/kubernetes-sigs/aws-efs-csi-driver/pull/464), [@devinsmith911](https://github.com/devinsmith911))


# v2.0.0

## Breaking changes

Multiple changes in values file at `sidecars`, `controller` and `node`

---
```yaml
sidecars:
  xxxxxxxxx:
    repository:
    tag:
```

Moving to

```yaml
sidecars:
  xxxxxxxxx:
    image:
      repository:
      tag:
```

---
```yaml
podAnnotations:
resources:
nodeSelector:
tolerations:
affinity:
```

Moving to

```yaml
controller:
  podAnnotations:
  resources:
  nodeSelector:
  tolerations:
  affinity:
```

---
```yaml
hostAliases:
dnsPolicy:
dnsConfig:
```

Moving to

```yaml
node:
  hostAliases:
  dnsPolicy:
  dnsConfig:
```

---
```yaml
serviceAccount:
  controller:
```

Moving to

```yaml
controller:
  serviceAccount:
```

## New features

* Chart API `v2` (requires Helm 3)
* Set `resources` and `imagePullPolicy` fields independently for containers
* Set `logLevel`, `affinity`, `nodeSelector`, `podAnnotations` and `tolerations` fields independently
for Controller deployment and Node daemonset
* Set `reclaimPolicy` and `volumeBindingMode` fields in storage class

## Fixes

* Fixing Controller deployment using `podAnnotations` and `tolerations` values from Node daemonset
* Let the user define the whole `tolerations` array, default to `- operator: Exists`
* Default `logLevel` lowered from `5` to `2`
* Default `imagePullPolicy` everywhere set to `IfNotPresent`