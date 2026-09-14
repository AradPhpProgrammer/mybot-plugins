# MyBot Templates Directory

This folder contains verified, ready-to-import JSON flow templates for **MyBot Studio**.

## Available Templates

### 1. `ai-agent/openai-assistant.json`
- **Purpose**: Fully functional AI chat assistant bot.
- **Features**:
  - Welcomes users on `/start`
  - Captures any text message via `$payload`
  - Sends a secure HTTP POST request to an LLM API endpoint (OpenAI, DeepSeek, OpenRouter)
  - Saves the result in the custom variable `$ai_reply`
  - Replies to the user with the generated text

## How to use:
1. Open your MyBot Studio dashboard.
2. Go to **Bot Settings** -> **Template Builder (Export / Import)**.
3. Click **Import JSON** and select any `.json` file from this repository.
4. Customize your API keys and parameters on the canvas!