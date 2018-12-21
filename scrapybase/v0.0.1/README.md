## Prerequisites

- Kubernetes 1.4+ with Beta APIs enabled
- PV provisioner support in the underlying infrastructure

## Configuration

The following table lists the configurable parameters of the scrapybase chart and their default values.

|         Parameter                   |             Description                    |                         Default                          |
|----------------------------         |-------------------------------------       |----------------------------------------------------------|
| `image.registry`                    | Image registry                             | `reg.bcc-agi.local/library/alpine-crawlbase`             |
| `image.repository`                  | Image name                                 | `scrapy0.2_20181220`                                     |
| `image.tag`                         | Image tag                                  | `{VERSION}`                                              |
| `image.pullPolicy`                  | Image pull policy                          | `Always` if `imageTag` is `latest`, else `IfNotPresent`  |
| `persistence.mountPath`             | Specify image nfs image                    | `/app`                                                   |
| `persistence.mountName`             | ProjectName                                | `fold and projectname`                                   |
| `persistence.claimName`             | NFS ClaimName                              | `crawlappclaim`                                          |
 
```bash
$ helm install --name my-release -f values.yaml stable/image
```
 