Quickly get started with Ollama, a tool for running large language models locally, with this cheat sheet. Install Ollama on your preferred platform (even on a Raspberry Pi 5 with just 8 GB of RAM), download models, and customize them to your needs. Ollama is a tool that allows you to run open-source large language models (LLMs) locally on your machine.
## Quick start Guide
### Installation

- **macOS**: [Download Ollama for macOS](https://ollama.com/download/Ollama-darwin.zip)
- **Windows (Preview)**: [Download Ollama for Windows](https://ollama.com/download/OllamaSetup.exe)
- **Linux**:
  ```bash
  curl -fsSL https://ollama.com/install.sh | sh
  ```
  [Manual Install Instructions for Linux](https://github.com/jmorganca/ollama/blob/main/docs/linux.md)
- **Docker**: Official image available at `ollama/ollama` on [Docker Hub](https://hub.docker.com/r/ollama/ollama)

### Libraries

- Python: [ollama-python](https://github.com/ollama/ollama-python)
- JavaScript: [ollama-js](https://github.com/ollama/ollama-js)

### Quickstart

Run and chat with Llama 2:
```bash
ollama run llama2
```

### Model Library

Access a variety of models from [ollama.com/library](https://ollama.com/library). Example commands to download and run specific models:
- `ollama run llama2`
- `ollama run mistral`
- `ollama run dolphin-phi`

## Customize a Model

### Import Models

- **GGUF**: Use a `Modelfile` with the `FROM` instruction pointing to the GGUF file.
  ```bash
  FROM ./model.gguf
  ollama create mymodel -f Modelfile
  ollama run mymodel
  ```
- **PyTorch/Safetensors**: Refer to the [import guide](docs/import.md).

### Customize Prompt

1. Pull the model:
   ```bash
   ollama pull llama2
   ```
2. Create a `Modelfile` with custom parameters and system messages.
3. Create and run the model:
   ```bash
   ollama create custommodel -f ./Modelfile
   ollama run custommodel
   ```


## Advanced usage
### CLI Reference

- **Create a model**: `ollama create mymodel -f ./Modelfile`
- **Pull a model**: `ollama pull modelname`
- **Remove a model**: `ollama rm modelname`
- **Copy a model**: `ollama cp source_model new_model`
- **List models**: `ollama list`
- **Start Ollama (without GUI)**: `ollama serve`

### Multimodal Input

- **Text**: Wrap multiline input with `"""`.
- **Images**: Specify the image path directly in the prompt.

### REST API Examples

- **Generate a response**:
  ```bash
  curl http://localhost:11434/api/generate -d '{"model": "llama2", "prompt":"Why is the sky blue?"}'
  ```
- **Chat with a model**:
  ```bash
  curl http://localhost:11434/api/chat -d '{"model": "mistral", "messages": [{"role": "user", "content": "why is the sky blue?"}]}'
  ```

Refer to the [API documentation](https://github.com/ollama/ollama/blob/main/docs/api.md) for more details.
