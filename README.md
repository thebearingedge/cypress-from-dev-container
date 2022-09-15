# cypress-from-dev-container

Getting Cypress GUI running from within an Ubuntu docker container on macOS and Windows. Linux pending.

```jsonc
// .devcontainer/devcontainer.json
{
  "containerEnv": {
    "DISPLAY": "host.docker.internal:0" // Docker Desktop DNS for host machine
  }
}
```

X.Org for Windows and macOS is provided by [XQuartz]() and [VcXsrv](), respectively.

## Windows

- Install `VcXsrv`
- ...launch and config
- clone repo into VS Code

## macOS

- Install `XQuartz`
- ...launch and config
- clone repo into VS Code
