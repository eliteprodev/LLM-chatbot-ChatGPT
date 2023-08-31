# LLM-chatbot-ChatGPT

Features:

* WebSocket chatbot server
* Docker-friendly
* Sample web and CLI clients provided
* Pluggable LLM backends (currently OpenAI API with ChatGPT or GPT-4)
* Out-of-the-box support for ChatGPT plugins
* ChatGPT plugin auth methods supported: `none`, `user_http`, `service_http`
* Request validation for the plugins according to their OpenAPI specifications
* Prompt customization for fine-grained instructions.

## Quick Start

1. Install Python 3.10, if not already installed.
2. Clone this repository.
3. Navigate to the cloned repository directory: `cd horace`
4. Create a new virtual environment: `python3 -m venv ./venv`
5. Activate the virtual environment: `source ./venv/bin/activate`
6. Install project requirements: `pip3 install -r requirements.txt`
7. Navigate to the `app` directory: `cd app`
8. Start the server: `OPENAI_API_KEY=openai-api-key python3 main.py` (replace `openai-api-key` with your OpenAI API key - get it [here](https://platform.openai.com/signup))
9. Launch a client:
  * For the CLI client, run this in another terminal window:

## Running via Docker

1. Clone this repository.
2. Navigate to the cloned repository directory: `cd horace`
3. Build the Docker image: `docker build -t horace:latest .`
4. Start the server:
```
docker run --rm \
  -e OPENAI_API_KEY=openai-api-key \
  -p 8001:8001 \
  --name horace \
  horace:latest
```
5. Launch a client:
  * For the CLI client, run this in another terminal window: `docker exec -it horace python3 /app/horace-cli.py`
  * For the web client, double-click `client-demo/index.html` in Explorer/Finder etc. to open it in your browser.

## Running Tests

Tests have not yet been updated since forking from GRACE. To be fixed.
