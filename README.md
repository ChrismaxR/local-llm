# RAG Application README

## Overview
This application, developed with Python and LangChain, leverages the Retriever-Augmented Generation (RAG) methodology to interact with various local Large Language Models (LLMs) provided by Ollama, such as gemma:2b, llama2, and mistral. It is designed to ingest multiple Word documents, process these documents by splitting them into manageable chunks, and convert these chunks into embeddings. This setup allows users to pose questions to the embedded content, which are then answered by the integrated LLMs, facilitating a powerful, localized, and versatile NLP tool.

## Features
- **Document Ingestion**: Batch process Word documents to extract text.
- **Chunk Splitting**: Break down the document text into smaller, manageable chunks.
- **Embeddings Conversion**: Convert text chunks into vector embeddings for efficient querying.
- **Question Answering**: Utilize local LLMs to pose questions to and receive answers based on the document embeddings.

## Requirements
- Python 3.9.18
- LangChain
- Ollama LLMs (gemma:2b, llama2, mistral)
- Any additional Python libraries as specified in `requirements.txt`.

## Installation

1. Clone this repository to your local machine.
2. Install the required Python packages:

```bash
pip install -r requirements.txt
```

3. Download and configure your local LLMs as per the documentation provided by Ollama.

## Usage

To run the application, execute the following command from the terminal:

```bash
python rag_application.py --docs_path "path/to/your/documents"
```

### Parameters
- `--docs_path`: Directory path containing the Word documents to be processed.

## How It Works
1. **Document Ingestion**: The application first ingests the specified Word documents from the provided directory.
2. **Chunk Splitting**: Each document is then split into chunks, with a default size that can be adjusted based on user preference or document complexity.
3. **Embeddings Conversion**: These chunks are converted into embeddings using the specified LLM's embedding capabilities.
4. **Question Answering**: Users can pose questions via a simple interface, which the application routes to the most relevant LLM based on the embeddings.

## Contributing
Contributions to enhance the application are welcome. Please fork the repository, make your changes, and submit a pull request for review.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- The developers of Python and LangChain for their invaluable tools.
- Ollama for providing access to cutting-edge local LLMs.
- Santiago Valdarrama's video's on buidling RAG applications and using open-sourced models (https://youtu.be/BrsocJb-fAo and https://youtu.be/HRvyei7vFSM). See also Santiago's github page: https://github.com/svpino
- Thu Vu inspired me to check out Local LLM's: https://github.com/thu-vu92 and https://youtu.be/h_GTxRFYETY?si=biEUfjGNLtNqixWM
