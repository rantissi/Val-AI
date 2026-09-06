# Free AI Models

Val can be used with free AI models available through OpenRouter.

The list below contains some of the currently available free models. OpenRouter may add, remove, or change free models over time, so always check the official model list before deploying.

## Recommended Models

| Model                         | Model ID                             | Best For                                  |
| ----------------------------- | ------------------------------------ | ----------------------------------------- |
| NVIDIA Nemotron 3.5 Lightning | `nvidia/nemotron-3.5-lightning:free` | Fast conversations and general use        |
| Google Gemma 4 31B            | `google/gemma-4-31b-it:free`         | General conversation and reasoning        |
| Google Gemma 4 26B A4B        | `google/gemma-4-26b-a4b-it:free`     | Fast general-purpose conversations        |
| OpenAI GPT-OSS 20B            | `openai/gpt-oss-20b:free`            | Reasoning and general tasks               |
| NVIDIA Nemotron 3 Super       | `nvidia/nemotron-3-super:free`       | Reasoning and complex tasks               |
| MiniMax M3                    | `minimax/minimax-m3:free`            | General conversation and multimodal tasks |

## Automatic Free Model Selection

OpenRouter also provides a free model router:

```text
openrouter/free
```

Instead of choosing a specific model, the router automatically selects an available free model based on the capabilities required by the request.

This can be useful if you don't want to manually update the model whenever OpenRouter changes its free model lineup.

## Using a Free Model

In your API request, set the model to one of the available free model IDs.

Example:

```javascript
const CONFIG = {
  API_URL: "https://openrouter.ai/api/v1/chat/completions",
  MODEL: "nvidia/nemotron-3.5-lightning:free"
};
```

Or use the automatic router:

```javascript
const CONFIG = {
  API_URL: "https://openrouter.ai/api/v1/chat/completions",
  MODEL: "openrouter/free"
};
```

## Important Notes

Free models are intended for experimentation, development, and low-volume usage. They may have lower rate limits, availability can vary, and specific models may be removed or replaced.

OpenRouter currently documents `:free` variants as free models with low rate limits.

For the most up-to-date list, check the OpenRouter model browser:

[OpenRouter Free Models](https://openrouter.ai/models?pricing=free&utm_source=chatgpt.com)

## Choosing a Model for Val

For a conversational AI like Val, a good starting point is:

```text
nvidia/nemotron-3.5-lightning:free
```

If you want Val to automatically switch between available free models, use:

```text
openrouter/free
```

Keep in mind that free model availability and limits can change, so the model list in this file should be treated as a snapshot rather than a permanent list.
