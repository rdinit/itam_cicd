# itam_cicd

Inputs:
- `registry-url` url for container registry example: `ghcr.io/octocat`
- `registry-username` string which provided as username to docker
- `registry-password`: password (or auth token for some container registries)
- `image-name` image name and tag, for example `imeage:latest`


Example:

```yml
name: Build example

on:
  workflow_dispatch

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Build and push
        uses: rdinit/itam_cicd@v1
        with:
          registry-url: ghcr.io/octocat
          registry-username: octocat
          registry-password: password 
          image-name: imeage:latest
```
