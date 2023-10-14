# Latex development using Docker and VSCode Remote Containers

Installation and configuration of LaTeX is both time and data heavy and also prone to easy misconfiguration.
Packaging the whole thing up in a container and then developing inside it using VSCode remote containers extension seems to be a simpler solution.

> In this example, a public docker image that's built from the file `.devcontainer/Dockerfile.TexLive` is used to launch the development container.
> To instead build a container from scratch and use it locally, change `dockerFile` in `.devcontainer/devcontainer.json` from `Dockerfile` to `Dockerfile.TexLive`

## Steps

1. Install [Docker Desktop](https://www.docker.com/products/docker-desktop)
2. Install [VS Code Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension for VSCode.
3. Install [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) extension for VSCode.
4. Open this directory.
5. Execute `Remote-Containers: Reopen in Container` in the VS Code Command Palette. This will start building the docker image. It takes some time to finish as the container is close to 7GB due to the huge TexLive installation size.
6. Open 'sample.tex' and start the compilation by clicking the green play button in the top right corner of VSCode.
7. Once it compiles without errors, the output PDF file should be in the same directory under the same name.

> The devcontainer.json defines LaTeX specific settings and extensions for VSCode.
