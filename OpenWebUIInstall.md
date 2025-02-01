Run open-webui https://github.com/open-webui/open-webui
This is the simple web ui that can interact with the LLM https://docs.openwebui.com eg. for locally installed LLM

use uv (https://docs.astral.sh/uv/concepts/tools/#including-additional-dependencies, a python package manager) commandline to install documented in "Installation with uv" in https://docs.openwebui.com because if local python 3 is 3.13, cannot use pip to install open-webui, only supported 3.11 python as of 01/25/2025
```
curl -LsSf https://astral.sh/uv/install.sh | sh
source $HOME/.local/bin/env (sh, bash, zsh)
source $HOME/.local/bin/env.fish (fish)
export DATA_DIR=~/.open-webui
uvx --python 3.11 open-webui@latest serve
```
uv command list is here https://docs.astral.sh/uv/pip/inspection/
You can use uv to manage multiple python version in your local environment see this doc for details https://docs.astral.sh/uv/concepts/python-versions/ this is needed when sometimes the software only works on certain version of python

Do the following to add to PATH and environment variable so next time open terminal, you can just run one command:uvx --python 3.11 open-webui@latest serve
```
In your home directory, if no .profile, just create one using touch .profile
then
echo "source $HOME/.local/bin/env" >>.profile
echo "export DATA_DIR=~/.open-webui" >>.profile
```
open web-ui will be at http://localhost:8080

Once you finish the installation once, in the future, you only need to:
```
1. start it
uvx --python 3.11 open-webui@latest serve
2. access it
http://localhost:8080
```

The following is not needed, docker instruction, TODO update this one
```
brew install --cask docker
or
https://docs.docker.com/desktop/setup/install/mac-install/

The following docker command assumes ollama is on the local machine

docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```
