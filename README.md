# RAG Memory Layer

![rag](https://img.shields.io/badge/rag-blue?style=flat-square) ![memory](https://img.shields.io/badge/memory-blue?style=flat-square) ![vector-db](https://img.shields.io/badge/vector--db-blue?style=flat-square)

A dedicated memory layer for agents using semantic search over previous interactions.

## Overview
The **RAG Memory Layer** provides a high-performance retrieval system designed to give AI agents long-term persistence. By indexing past conversations and interactions into a vector database, it enables agents to recall relevant historical context through semantic search. This ensures that agentic workflows remain consistent and contextually aware over extended periods.

## Features
*   **Semantic Retrieval:** Efficiently query past interactions based on meaning rather than just keywords.
*   **Vector Database Integration:** Built-in support for industry-standard vector stores for scalable storage.
*   **Contextual Ranking:** Automatically ranks and surfaces the most relevant memories for the current prompt.
*   **Lightweight API:** Designed for easy integration into existing Python-based agent frameworks and RAG pipelines.

## Installation
Ensure you have Python installed, then clone the repository and install the necessary dependencies:

```bash
git clone https://github.com/yourusername/rag-memory-layer.git
cd rag-memory-layer
pip install -r requirements.txt
```

## Usage
To start the memory layer and store/retrieve interactions, run the main entry point:

```bash
python main.py
```

**Quick Example:**
```python
from memory_layer import RagMemory

# Initialize memory
memory = RagMemory()

# Save an interaction
memory.add("User asked about project deadlines on Friday.")

# Retrieve context
context = memory.search("When is the project due?")
print(context) 
# Output: "User asked about project deadlines on Friday."
```

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change. Ensure that your code adheres to the existing style and includes appropriate documentation.

## License
This project is licensed under the [MIT License](LICENSE).