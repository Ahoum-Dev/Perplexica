# Perplexica Environment Variables for Coolify

## Required Environment Variables

Copy these environment variables into your Coolify service configuration:

### General Configuration
```bash
SIMILARITY_MEASURE=cosine
KEEP_ALIVE=5m
```

### API Keys (Add only the ones you plan to use)

#### Groq (You already have this)
```bash
GROQ_API_KEY=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
```

#### OpenAI (Optional - only if you want to use GPT models)
```bash
OPENAI_API_KEY=sk-your-openai-key-here
```

#### Anthropic (Optional - only if you want to use Claude models)
```bash
ANTHROPIC_API_KEY=your-anthropic-key-here
```

#### Google Gemini (Optional)
```bash
GEMINI_API_KEY=your-gemini-key-here
```

#### DeepSeek (Optional)
```bash
DEEPSEEK_API_KEY=your-deepseek-key-here
```

### Local LLM Configuration (Optional)

#### Ollama (if you have Ollama running)
```bash
OLLAMA_API_URL=http://your-ollama-host:11434
```

#### LM Studio (if you use LM Studio)
```bash
LM_STUDIO_API_URL=http://your-lm-studio-host:1234
```

### Custom OpenAI Configuration (Optional)
```bash
CUSTOM_OPENAI_API_KEY=your-custom-api-key
CUSTOM_OPENAI_API_URL=https://your-custom-openai-endpoint.com
CUSTOM_OPENAI_MODEL_NAME=your-model-name
```

### API Endpoints (Optional)
```bash
SEARXNG_ENDPOINT=http://localhost:32768
```

## How to Set These in Coolify

1. **Go to your Perplexica service in Coolify**
2. **Navigate to "Environment Variables" tab**
3. **Add each variable one by one**:
   - Click "Add Variable"
   - Enter the variable name (e.g., `GROQ_API_KEY`)
   - Enter the value
   - Click Save

4. **Required vs Optional**:
   - **Required**: `SIMILARITY_MEASURE`, `KEEP_ALIVE`
   - **At least one API key**: `GROQ_API_KEY` (you already have this)
   - **Optional**: All other variables based on your needs

## Minimum Setup

For a basic working setup, you only need:
```bash
SIMILARITY_MEASURE=cosine
KEEP_ALIVE=5m
GROQ_API_KEY=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
```

## Security Note

✅ **Good**: Environment variables in Coolify are encrypted and secure
❌ **Never**: Put API keys in your git repository
🔒 **Best Practice**: Use different API keys for development and production 