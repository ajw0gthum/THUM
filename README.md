# THUM - Personal AI Projects

This repository contains personal AI projects integrating with OpenRoute AI.

## Setup

### Prerequisites
- OpenRouter API key (get one at https://openrouter.io)

### Node.js Setup

1. Navigate to the `nodejs` directory:
```bash
cd nodejs
npm install
```

2. Create a `.env` file in the nodejs directory:
```bash
cp ../.env.example .env
# Edit .env and add your OpenRouter API key
```

3. Run the example:
```bash
npm start
```

### Python Setup

1. Navigate to the `python` directory:
```bash
cd python
```

2. Create a `.env` file in the python directory:
```bash
cp ../.env.example .env
# Edit .env and add your OpenRouter API key
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Run the example:
```bash
python example_usage.py
```

## Available Models

Some popular models available through OpenRouter:
- `openai/gpt-4` - GPT-4
- `openai/gpt-3.5-turbo` - GPT-3.5 Turbo
- `anthropic/claude-2` - Claude 2
- `meta-llama/llama-2-70b-chat` - Llama 2
- `mistralai/mistral-7b-instruct` - Mistral

For a full list, visit: https://openrouter.io/docs/models

## Usage

### Node.js Example

```javascript
const OpenRouteClient = require('./openroute-client');

const client = new OpenRouteClient();
const response = await client.chat('openai/gpt-3.5-turbo', 'Hello!');
console.log(response);
```

### Python Example

```python
from openroute_client import OpenRouteClient

client = OpenRouteClient()
response = client.chat('openai/gpt-3.5-turbo', 'Hello!')
print(response)
```

## API Parameters

Both clients support:
- `temperature` - Controls randomness (0-2, default: 0.7)
- `max_tokens` - Maximum response length (default: 2048)
- Additional parameters can be passed via `**options`

## Documentation

- [OpenRouter API Docs](https://openrouter.io/docs)
- [Chat Completions API](https://openrouter.io/docs/api/completions)

## License

Apache License 2.0
