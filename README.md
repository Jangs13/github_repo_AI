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

- OPENAI_API_KEY=your_openai_api_key
- GITHUB_TOKEN=your_github_token
- ACTIVELOOP_TOKEN=your_activeloop_token
- DATASET_PATH=your_deeplake_dataset_path

Usage
Run the main script:

```bash
python main.py
```

Enter the GitHub repository URL when prompted.

The script will load the data from the specified repository, upload it to the DeepLake vector store, and initialize a query engine.

You can ask questions about the repository data. 

## Example

Please enter the GitHub repository URL: https://github.com/soos3d/chatgpt-plugin-development-quickstart-express 

Loading chatgpt-plugin-development-quickstart-express repository by soos3d 

Documents uploaded:
{'file_path': 'README.md', 'file_name': 'README.md'}
{'file_path': 'index.js', 'file_name': 'index.js'}
{'file_path': 'src/app.js', 'file_name': 'app.js'}

Uploading to vector store...

Your Deep Lake dataset has been successfully created!

Dataset(path='hub://YOUR_ORG/repository_db', tensors=['embedding', 'id', 'metadata', 'text'])

| tensor     | htype      | shape     | dtype   | compression |
|------------|------------|-----------|---------|-------------|
| embedding  | embedding  | (5, 1536) | float32 | None        |
| id         | text       | (5, 1)    | str     | None        |
| metadata   | json       | (5, 1)    | str     | None        |
| text       | text       | (5, 1)    | str     | None        |

   
Test question: What is the repository about?

'''=================================================='''

Answer: The repository is a ChatGPT Plugin Quickstart with Express.js. It provides a foundation for
developing custom ChatGPT plugins using JavaScript and Express.js. The sample plugin in the
repository showcases how ChatGPT can integrate with external APIs, specifically API-Ninja's API, to
enhance its capabilities. The plugin fetches airport data based on a city name provided by the user.

Please enter your question (or type 'exit' to quit): how does the server work?

Your question: how does the server work?

'''=================================================='''

Answer: The server in this context works by setting up an Express.js server with various endpoints to serve
a ChatGPT plugin. It initializes the server, configures it to parse JSON in the body of incoming
requests, and sets up routes for serving the plugin manifest, OpenAPI schema, logo image, and
handling API requests. It also defines a catch-all route to handle any other requests. Finally, the
server starts and listens for requests on the specified port.

Please enter your question (or type 'exit' to quit): exit

Exiting, thanks for chatting!

## Notes

- Make sure you have sufficient OpenAI credits to use the GPT model.
- Ensure that your .env file is correctly configured with all necessary API keys and tokens.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](https://github.com/Jangs13/github_repo_AI?tab=MIT-1-ov-file)
 file for details.

