# Description
Integrate LLM models using LLM Studio with Open WebUI

## Deployment

 Follow the next steps to integrate [LLM Studio](https://lmstudio.ai/) with [Open WebUI](https://openwebui.com/)

- **STEP01**: Download LLM Studio and install
Install LLM Studio in Ubuntu 24.02. Download [LLM Studio for your architecture](https://lmstudio.ai/). In this case you will download a AppImage file. Copy this file under `/opt/LMStudio`, set some priviledges:

$ chown own simur:simur /opt/LMStudio
$ chmod +x /opt/LMStudio/LM_Studio.AppImage

Also download a LLM Studio icon `lmstudio.png` inside this repo under the same AppImage file folder.

- **STEP02**: Create a file launcher called `llm-studio.desktop` under `~/.local/share/applications` like this:

```
[Desktop Entry]
Name=LM Studio
Comment=LM Studio Launcher
Exec=/opt/LMStudio/LM_Studio.AppImage --no-sandbox
Icon=/opt/LMStudio/lmstudio.png
Terminal=false
Type=Application
Categories=Development;
StartupWMClass=LM Studio
```

- **STEP03**: Install a LLM Model and Load
Now we can start LLM Studio, and download our first LLM model to be used. Click in `LM Runtime` localed at left top and select a model to be downloaded and later loaded. In this case we select the model called [openai/gpt-oss-20b)](https://lmstudio.ai/models/openai/gpt-oss-20b). 

![LLM Studio Model Manager](./images/llm_model_download.png "LLM Studio Model Manager")

After be download we can load it. If we go to Developer menu option we see our model loaded

![LLM Studio Model Loaded](./images/llm_model_loaded.png "LLM Studio Model Loaded")

- **STEP04**: Start LLM Server and configure

Now with a LLM Model loaded, we can start our LLM Server. LLM Studio start a App icon menu at top of ubuntu.

![LLM Studio Icon Manager](./images/llm_studio_icon_manager.png "LLM Studio Icon Manager")

Now we configure this new LLM Server from LLM Studio. Go again to Developer LLM Studio and click `Server Settings` and set this options:

![LLM Studio Server Configuration](./images/llm_studio_server_configuration.png "LLM Studio Server Configuration")

With these options we can accedd to the LLM Server with port 1234 externally