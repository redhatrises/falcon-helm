# CrowdStrike Falcon Helm Repository

<br><br>
### Add the CrowdStrike Falcon Helm repository

```
helm repo add crowdstrike https://redhatrises.github.io/falcon-helm
```

<br>
### Update the local Helm repository Cache

```
helm repo update
```

<br>
### Install CrowdStrike Falcon Helm Chart

Install the CrowdStrike Falcon Helm Chart by running:
```
helm upgrade --install falcon-helm redhatrises/falcon-sensor \
    -n falcon-system --create-namespace \
    --set falcon.cid="<CrowdStrike_CID>" \
    --set node.image.repository="<Your_Registry>/falcon-node-sensor"
```

You can also install the CrowdStrike Falcon Helm Chart with the release name `falcon-helm` in the namespace your `kubectl` context is currently set to by running the following:

```
helm upgrade --install falcon-helm redhatrises/falcon-sensor \
    --set falcon.cid="<CrowdStrike_CID>" \
    --set node.image.repository="<Your_Registry>/falcon-node-sensor"
``` 

For more details please see the [falcon-helm](https://github.com/CrowdStrike/falcon-helm) repository.
