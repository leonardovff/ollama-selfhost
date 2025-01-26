## docker compose
```
docker compose up -d ollama
```

## client
```
echo "alias ollama='docker exec -it ollama ollama'" >> ~/.bashrc
```

### just docker
### if gpu
```
docker run -d --restart always --gpus=all -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

### without gpu
```
docker run -d --restart always -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

