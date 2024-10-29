---
aliases:
  - OpenWebUI
up:
  - [[MLOps]]
---
up:  [[MLOps]]

# OpenWebUI
Open Web UI ; openwebui
(used with [[#Ollama]])  
OpenWebUI - This is a specific web UI framework designed for building and deploying LLM applications (C) Gemini


ВАЖНО: https://docs.openwebui.com/getting-started/ ; https://docs.openwebui.com/




#### Install
https://docs.openwebui.com/getting-started/

If Ollama is on your computer, use this command:
docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main

только chatgpt


#### docker install
docker pull ghcr.io/open-webui/open-webui:main

https://hub.docker.com/r/backplane/open-webui
docker pull backplane/open-webui



