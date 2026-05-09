# EUopenDataStack

## Aim
A free and open source scalable data stack that does not depend on Cloud infrastructure. All components are able to run on affordalbe HW, no GPU involved.

##Install the Stack
# Ollama
See https://ollama.com/download

To download and install Ollama run 
```bash
curl -fsSL https://ollama.com/install.sh | sh
```
verify installation
```bash
ollama -v 
```

# LLM
The LLM can be served directly via ollama. There are various smaller models that run directly on local HW without the need of GPUs. Of course, their performance is far from the bigger models, but with the correct instructions and context, these models can handle almost every instruction on smaller data sets.
I use the Mistral 3 3B model: https://mistral.ai/news/mistral-3
https://ollama.com/library/ministral-3:3b

Pull the model:
```bash
ollama pull ministral-3:3b
```
Run the model
```bash
ollama run ministral-3:3b
```




