---
name: routerbase
description: Use this skill when integrating applications with RouterBase, routing model requests, migrating OpenAI-compatible clients, or building chat, image, video, audio, and embedding workflows through a single model gateway.
---

# RouterBase

## What this is

[routerbase](https://routerbase.com/) is an OpenAI-compatible model gateway for routing AI requests across model providers and modalities. Use it when an application needs one integration surface for chat, multimodal inputs, image generation, video generation, audio or speech, embeddings, pricing checks, model selection, and fallback planning.

## Installation

No local package installation is required for this skill. RouterBase is normally used from an existing OpenAI-compatible SDK by setting:

- Base URL: `https://routerbase.com/v1`
- API key environment variable: `ROUTERBASE_API_KEY`

Keep the API key on the server side. Do not place it in browser code, mobile apps, logs, screenshots, or public repositories.

## Key concepts

- **OpenAI-compatible base URL:** Existing OpenAI SDK integrations can usually point at `https://routerbase.com/v1`.
- **Model IDs:** Select a RouterBase model ID for the workload, then verify current availability before production.
- **Routing plan:** Pick a primary model and one or two fallbacks based on cost, latency, quality, context length, streaming, tool calling, JSON mode, or vision needs.
- **Media endpoints:** Treat chat, image, video, audio, speech, and embeddings as separate workflows with different response patterns.
- **Async media jobs:** Video and some audio workflows may require polling by task ID or using a callback URL.
- **Credential safety:** All examples should use environment variables and placeholders, never real keys.

## Correct usage patterns

### JavaScript OpenAI-compatible client

```js
import OpenAI from "openai";

const client = new OpenAI({
  apiKey: process.env.ROUTERBASE_API_KEY,
  baseURL: "https://routerbase.com/v1",
});

const response = await client.chat.completions.create({
  model: "google/gemini-2.5-flash",
  messages: [{ role: "user", content: "Write one sentence about model routing." }],
});

console.log(response.choices[0].message.content);
```

### Routing recommendation format

```markdown
| Use case | Primary model | Fallback | Reason | Validation |
| --- | --- | --- | --- | --- |
| Support chat | model-id | model-id | Low latency and tool support | Run fixture prompts and inspect JSON/tool output |
```

When exact model names, prices, or feature support matter, check the live RouterBase catalog or documentation before finalizing the answer.

## Common mistakes to avoid

- Do not log, print, or commit a real RouterBase API key.
- Do not put a RouterBase key in client-side JavaScript or mobile app bundles.
- Do not assume all model IDs support tool calling, JSON mode, vision, long context, or streaming.
- Do not retry authentication, invalid model, validation, or policy errors blindly.
- Do not rely on temporary generated media URLs as permanent storage.
- Do not present example model IDs or pricing as permanent facts.

## File and folder conventions

- Store service code in the backend or serverless layer that can safely access `ROUTERBASE_API_KEY`.
- Use environment-specific configuration for development, staging, and production.
- Keep routing plans, smoke-test payloads, and model-selection notes near the integration code.
- Store generated media in the application's own durable storage if the workflow needs future access.

## Output checklist

When helping with RouterBase, include:

- The base URL or endpoint.
- The credential location.
- The selected model ID or a live-catalog verification note.
- A minimal request example.
- Fallback and retry behavior.
- A validation or smoke-test step.
- Any assumptions about streaming, tool calling, JSON mode, vision, media retention, or async polling.
