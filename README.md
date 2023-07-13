# Validated Pattern Utility Container

utility container for simplified execution of imperative commands in each of the patterns.


## Installed Software

|               name                |  type    |   version    |
|:---------------------------------:|:--------:|:------------:|
|ansible                            |pip       |2.15.1        |
|argocd                             |binary    |v2.5.7+e0ee345|
|awscli                             |pip       |1.29.3        |
|azure-cli                          |pip       |2.50.0        |
|boto3                              |pip       |1.28.3        |
|botocore                           |pip       |1.31.3        |
|gcloud                             |pip       |0.18.3        |
|git-core                           |package   |2.39.3        |
|helm                               |binary    |v3.10.3       |
|jq                                 |package   |1.6           |
|kubernetes.core                    |collection|2.4.0         |
|kubernetes                         |pip       |26.1.0        |
|kustomize                          |binary    |v4.5.4        |
|make                               |package   |4.3           |
|openshift                          |binary    |4.11.25       |
|python3-pip                        |package   |21.2.3        |
|python                             |package   |3.9.16        |
|redhat_cop.controller_configuration|collection|2.3.1         |
|sshpass                            |package   |1.09          |
|tar                                |package   |1.34          |
|tekton                             |binary    |0.29.0        |
|vi                                 |package   |8.2.2637      |

## Usage
**Pull the image**
```bash
podman pull quay.io/hybridcloudpatterns/utility-container:latest
```

**Use image to execute a playbook**
```bash
podman run -it --rm --net=host quay.io/hybridcloudpatterns/utility-container:latest ansible-playbook <playbook>.yml
```

## Build the image
Just run: `make build` and both amd64 and arm64 will be built locally (you will need the qemu-user-static package installed)

To upload the image to the official repository, run: `make UPLOADREGISTRY=quay.io/hybridcloudpatterns upload` (by default it uploads somewhere else
to try and avoid accidental uploads)

