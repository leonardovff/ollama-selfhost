# Ollama + open-webui self hosted with Docker

## Requirements
docker

## Installation
```
1. Up the ollama server using the docker
docker compose up -d ollama

2. Ollama client using docker in alias command 
echo "alias ollama='docker exec -it ollama ollama'" >> ~/.bashrc

3. Install the list of available models here:
https://github.com/ollama/ollama?tab=readme-ov-file#model-library
```

## If you prefer to use just docker cli
### if you want gpu
```
docker run -d --restart always --gpus=all -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

### if you want without gpu
```
docker run -d --restart always -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

