# GitHub Repo AI

This project is designed to load data from a GitHub repository, upload it to a DeepLake vector store, and allow querying using OpenAI's GPT model. It uses the `llama_index` and `deeplake` libraries for data processing and storage.

## Features

- Load data from a specified GitHub repository.
- Upload data to a DeepLake vector store.
- Query the data using OpenAI's GPT model.
- Handle various file extensions including `.py`, `.js`, `.ts`, and `.md`.

## Requirements

- Python 3.8+
- An OpenAI API key
- A GitHub token
- An Activeloop token
- The following Python packages:
  - `dotenv`
  - `llama_index`
  - `deeplake`
  - `httpx`
  - `PyYAML`
  - `SQLAlchemy`
  - `aiohttp`
  - `dataclasses-json`
  - `deprecated`
  - `dirtyjson`
  - `fsspec`
  - `llamaindex-py-client`
  - `nest-asyncio`
  - `networkx`
  - `nltk`
  - `numpy`
  - `openai`
  - `pandas`
  - `pillow`
  - `requests`
  - `tenacity`
  - `tiktoken`
  - `tqdm`
  - `typing-extensions`
  - `typing-inspect`
  - `wrapt`
  - `beautifulsoup4`
  - `pypdf`
  - `striprtf`
  - `aiosignal`
  - `attrs`
  - `frozenlist`
  - `multidict`
  - `yarl`
  - `async-timeout`
  - `soupsieve`
  - `pydantic`
  - `click`
  - `joblib`
  - `regex`
  - `distro`
  - `charset-normalizer`
  - `urllib3`
  - `greenlet`
  - `colorama`
  - `mypy-extensions`
  - `marshmallow`
  - `python-dateutil`
  - `pytz`
  - `tzdata`
  - `packaging`
  - `annotated-types`
  - `pydantic-core`
  - `six`

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Jangs13/Github-Repo-AI.git
   cd Github-Repo-AI
   
Install the required packages:

```bash
pip install -r requirements.txt
```

## Create a .env file in the root directory of the project and add the following environment variables:

.env

OPENAI_API_KEY=your_openai_api_key
GITHUB_TOKEN=your_github_token
ACTIVELOOP_TOKEN=your_activeloop_token
DATASET_PATH=your_deeplake_dataset_path

Usage
Run the main script:

```bash
python main.py
```

Enter the GitHub repository URL when prompted.

The script will load the data from the specified repository, upload it to the DeepLake vector store, and initialize a query engine.

You can ask questions about the repository data. 

## Example

Please enter the GitHub repository URL: https://github.com/Jangs13/Ray_Peat_Scrape_Search
Loading Ray_Peat_Scrape_Search repository by Jangs13
Documents uploaded:
{'file_path': 'app.py', 'file_name': 'app.py', 'url': 'https://github.com/Jangs13\\Ray_Peat_Scrape_Search\\blob/master\\app.py'}
{'file_path': 'pipeline.py', 'file_name': 'pipeline.py', 'url': 'https://github.com/Jangs13\\Ray_Peat_Scrape_Search\\blob/master\\pipeline.py'}
Uploading to vector store...
Test question: What is the repository about?
==================================================
Answer: This repository contains scripts for scraping and analyzing data related to Ray Peat.

## Notes

- Make sure you have sufficient OpenAI credits to use the GPT model.
- Ensure that your .env file is correctly configured with all necessary API keys and tokens.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

