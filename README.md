# Argo Dev Containers

> This repo provides a starting point and example for creating your own custom [Dev Containers](https://containers.dev), hosted on GitHub Container Registry.  

## Repo Structure

This repository contains a _collection_ of devcontainer images within the `src` folder.  Each image type has its own sub-folder, containing at least a `.devcontainer/devcontainer.json` file. 

```
├── src
│   ├── python
│   │   └──| .devcontainer
│   │      └── devcontainer.json
│   ├── universal
│   │   └──| .devcontainer
│   │      ├── devcontainer.json
|   ├── ...
│   │   └──| .devcontainer
│   │      ├── Dockerfile
           └── devcontainer.json
├── test
│   ├── python
│   │   └── test.sh
│   ├── universal
│   │   └── test.sh
│   └──test-utils
│      └── test-utils.sh
...
```

## Images

TODO

## Testing

TODO

This repo contains a GitHub Action [workflow](.github/workflows/test-pr.yaml) for testing the Templates. Similar to the [`devcontainers/templates`](https://github.com/devcontainers/templates) repo, this repository has a `test` folder.  Each Template has its own sub-folder, containing at least a `test.sh`.

For running the tests locally, you would need to execute the following commands -

```
    ./.github/actions/smoke-test/build.sh ${TEMPLATE-ID} 
    ./.github/actions/smoke-test/test.sh ${TEMPLATE-ID} 
```

## Publishing

TODO

This repo contains a GitHub Action [workflow](.github/workflows/release.yaml) that will automatically generate documentation (ie. `README.md`) for each Template. This file will be auto-generated from the `devcontainer-template.json` and `NOTES.md`.
