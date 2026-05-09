# EUopenDataStack

## Aim
A free and open source scalable data stack that does not depend on Cloud infrastructure. All components are able to run on affordalbe HW, no GPU involved.

## Install the Stack
### Ollama
See https://ollama.com/download

To download and install Ollama run 
```bash
curl -fsSL https://ollama.com/install.sh | sh
```
verify installation
```bash
ollama -v 
```

### LLM
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
If even smaller memory foortprints are required, a model like TinyLama can be utilized: https://ollama.com/library/tinyllama


### DuckDB
DuckDB is an open-source, high-performance, in-process SQL OLAP (Online Analytical Processing) database management system. It is frequently described as the "SQLite for analytics" because it is designed to be embedded directly into an application—such as a Python script, R environment, or CLI—without needing a separate server process.

Install DuckDB CLI with
```bash
curl https://install.duckdb.org | sh
```
launch DuckDB in your Home directory under 
```bash
<your home>/.duckdb/cli/latest/duckdb
```
follow the instructions under https://duckdb.org/docs/current/clients/cli/overview

As DuckDB works in process, it can directly be installed with the respective clients, described under https://duckdb.org/docs/current/clients/overview

Example, in Python, simply import DuckDB with
```python
pip install duckdb
import duckdb
```
For C#, there is the DuckDB.NET, which is a low level .Net wrapper around the DuckDB C API.



