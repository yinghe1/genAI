Use docker to run open-webui https://github.com/open-webui/open-webui
This is the simple web ui that can interact with the LLM https://docs.openwebui.com

use uv (https://docs.astral.sh/uv/concepts/tools/#including-additional-dependencies, a python package manager) commandline to install
```
curl -LsSf https://astral.sh/uv/install.sh | sh
source $HOME/.local/bin/env (sh, bash, zsh)
source $HOME/.local/bin/env.fish (fish)
export DATA_DIR=~/.open-webui
uvx --python 3.11 open-webui@latest serve
```
uv command list is here https://docs.astral.sh/uv/pip/inspection/

The following is not needed, docker instruction, TODO update this one
```
brew install --cask docker
or
https://docs.docker.com/desktop/setup/install/mac-install/

The following docker command assumes ollama is on the local machine

docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```
