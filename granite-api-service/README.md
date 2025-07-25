# Granite API Service (now using OpenRouter)

This service generates marketing content using the OpenRouter API (https://openrouter.ai/), replacing the previous IBM Granite integration.

## Environment Variables

Create a `.env` file in this directory with the following:

```
OPENROUTER_API_KEY=your_openrouter_api_key_here
OPENROUTER_MODEL=openai/gpt-4o
PORT=5000
```

- `OPENROUTER_API_KEY`: Your API key from https://openrouter.ai/
- `OPENROUTER_MODEL`: (Optional) The model to use, e.g., `deepseek/deepseek-r1:free` (default)
- `PORT`: (Optional) Port to run the service (default: 5000)

## Usage

Start the service:

```
npm install
npm start
```

The main endpoint is:

- `POST /api/dashboard/post` — Generates two marketing campaign variations and estimates metrics using OpenRouter.

## Notes
- This service no longer uses IBM/Granite models or authentication.
- All content and metrics estimation is now powered by OpenRouter-compatible models. 