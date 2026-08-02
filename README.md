# Silly Dataset Release Demo

This repository is a mock consumer project for
[`@shmuggingface/core`](https://github.com/ShmuggingFace/ShmuggingFaceCore).
It exists to prove that a normal dataset-producing repository can generate a
Cloudflare Pages review app before publishing a real Hugging Face or Kaggle
dataset.

The datasets are intentionally invented and harmless:

- **Sock Drawer Benchmark**: synthetic tabular rows about matching clean socks.
- **Office Mug Poses Mini**: synthetic computer-vision metadata about fake mug
  poses.
- **Elevator Small Talk Corpus**: tiny text snippets for awkward-weather-chat
  classification.

Generated pages are branded as ShmuggingFace and Shmaggle mocks and include a
visible notice that they are not real platform pages or real releases.

Live demo:
<https://shmuggingface-silly-dataset-demo-3rq.pages.dev/>

## Generate Locally

```sh
npm ci
npm run build
```

The static site is written to `dist/`.

## Deploy

The project is designed for Cloudflare Pages direct upload:

```sh
wrangler pages deploy dist --project-name shmuggingface-silly-dataset-demo --branch main
```

For closed review, protect the Pages hostname with Cloudflare Access outside
this repository. Do not commit reviewer emails, tokens, or provider payloads.
