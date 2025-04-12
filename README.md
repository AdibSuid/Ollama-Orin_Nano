
# Ollama-Orin_Nano

## Quick Start (Docker Container)

1. Clone jetson-container repository:
   ```bash
   git clone https://github.com/dusty-nv/jetson-containers.git

2. go to jetson-container directory:
   ```bash
   cd jetson-containers

3. Install the packages:
   ```bash
   bash install.sh

7. Run ollama docker container:
   ```bash
   jetson-containers run $(autotag ollama) /bin/ollama run phi3

Note: Start the Ollama command-line chat client with your desired model (for example: llama3 , phi3 , mistral )

##Native Installation

1. Install Ollama:
   ```bash
   curl -fsSL https://ollama.com/install.sh | sh
   
2. Run a model on CLI:
   ```bash
   ollama run llama3.2:3b
   
Note: Ollama service run on start up, so you can start using ollama command right away.

# Using Open WebUI

1. Run the command line below to install Open WebUI (run once, for the first setup only):
   ```bash
   sudo docker run -d --network=host \
   -v ${HOME}/open-webui:/app/backend/data \
   -e OLLAMA_BASE_URL=http://127.0.0.1:11434 \
   --name open-webui \
   --restart always \
   ghcr.io/open-webui/open-webui:main

2. Command line to run Open WebUI (need to run everytime wants to interact with LLM Model): 
   ```bash
   sudo docker start open-webui

3. Open your web browser and navigate to:
   ```bash
   http://localhost:8080/

4. Note: replace the "local host" with your own local ip address for example:
   ```bash
   http://192.168.68.117:8080/

5. Create an admin account by entering your name, email address, and a password. This account is stored locally on your device.
6. Click on the model selection menu and enter the model name (e.g., deepseek-r1:1.5b). This will initiate the download of the selected model to your local machine.
7. Simply type your queries into the chat window to interact with the Deepseek R1 model.
