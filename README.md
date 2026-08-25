# LLM Inference Speed Comparison

Same model, different provider, wildly different speed. Pick a model and see
who runs it fastest.

## What it shows

Output tokens per second for the same model across inference providers —
Cerebras, Groq, SambaNova, Fireworks AI, and first-party APIs. The model
weights are the same; the silicon and software stack are not.

7 models with multi-provider data, 18 entries total.

## Where the numbers come from

Three types, ranked by reliability:

- **Measured** — Artificial Analysis standardised benchmarks against live
  API endpoints. Most comparable.
- **Official** — from provider model catalogs and pricing pages. Real
  numbers but under the provider's own conditions.
- **Announced** — press releases (NVIDIA Groq 3 LPX, Cerebras Ultrafast).
  Not independently verified yet.

Each row carries its source and type so you can judge the number yourself.

## Notable gaps

These are the numbers that make the table worth looking at:

- **Gemma 4 31B**: NVIDIA Groq 3 LPX 3,400 tok/s vs SambaNova 204 = 16.7×
- **GPT OSS 120B**: Cerebras 3,000 vs Fireworks 70 = 42.9×
- **GPT-5.6 Sol**: Cerebras Ultrafast 750 vs OpenAI's own API 90 = 8.3×

## Deploy

Static site, no build step.

    vercel --prod

Framework preset **Other**, no build command, output directory `.`.

## Licence

MIT.
