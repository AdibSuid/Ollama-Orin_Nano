
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
