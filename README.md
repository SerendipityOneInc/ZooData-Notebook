# APIClaw Notebooks

Interactive Colab notebooks demonstrating [APIClaw](https://apiclaw.io) APIs — e-commerce intelligence and AI model endpoints.

## Getting Started

1. Sign up at [apiclaw.io/register](https://apiclaw.io/register) to get your API key (includes 1,000 free credits)
2. Click any **Open in Colab** badge below
3. Paste your API key when prompted

Need more credits for production workloads? See our [pricing plans](https://apiclaw.io/pricing).

## Notebooks

### E-Commerce Search

| Notebook | Description | APIs Used |
|----------|-------------|-----------|
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SerendipityOneInc/ZooData-Notebook/blob/main/e-commerce-search/product_search.ipynb) [Product Search](e-commerce-search/product_search.ipynb) | Find fashion products with natural-language queries. Covers brand, price, and retailer filtering. | `fashion-product-search` |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SerendipityOneInc/ZooData-Notebook/blob/main/e-commerce-search/image_search.ipynb) [Image Search](e-commerce-search/image_search.ipynb) | Visual similarity search — upload an image, find matching products. Includes detection, bounding-box cropping, text-guided search, "Shop the Look" pipeline, and direct SigLIP2 embeddings. | `fashion-image-search`, `image-detection`, `image-embedding`, `fashion-image-embedding`, `fashion-text-embedding`, `fashion-similarity` |

## The Model Behind the API: ZooClaw-FashionSigLIP2

APIClaw's fashion vision endpoints are powered by [**ZooClaw-FashionSigLIP2**](https://huggingface.co/srpone/zooclaw-fashionsiglip2) — our fashion-specialized SigLIP2 ViT-B/16 encoder producing 768-dim L2-normalized joint image/text embeddings. On our public [LookBench](https://github.com/SerendipityOneInc/look-bench) benchmark, it is currently the **best open-source fashion vision-language model** for brand, category, and fine-grained attribute matching.

📄 Paper: [*ZooClaw-FashionSigLIP2: Distilled Fine-tuning for Robust Fashion Retrieval*](https://arxiv.org/abs/2606.27708) (Xue & Xu, 2026)

> **The commercial API is even more robust than the open weights.** The endpoints below serve a continuously-updated production checkpoint — trained on additional proprietary fashion data, hardened with hard-negative mining, and retrained on a rolling schedule against fresh e-commerce catalog signals. Expect meaningfully stronger recall on rare brands, seasonal styles, and long-tail attributes than the public HuggingFace model — with zero infrastructure on your side.

Try the upgraded weights right now — no setup, no GPU:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SerendipityOneInc/ZooData-Notebook/blob/main/e-commerce-search/image_search.ipynb)

## API Reference

Full documentation: [apiclaw.io/api-docs](https://apiclaw.io/api-docs)

| Endpoint | Method | Description | Cost |
|----------|--------|-------------|------|
| `/openapi/v2/model/fashion-product-search` | POST | Text-based fashion product search across 200M+ items | 1 credit |
| `/openapi/v2/model/fashion-image-search` | POST | Visual similarity fashion product search | 1 credit |
| `/openapi/v2/model/image-detection` | POST | Detect fashion items → bounding boxes + category + confidence | 1 credit |
| `/openapi/v2/model/image-embedding` | POST | Detect + classify + generate feature embeddings (all-in-one) | 1 credit |
| `/openapi/v2/model/fashion-image-embedding` | POST | ZooClaw-FashionSigLIP2 768-dim image embeddings (batch up to 8) | 1 credit |
| `/openapi/v2/model/fashion-text-embedding` | POST | ZooClaw-FashionSigLIP2 768-dim text embeddings (batch up to 32) | 1 credit |
| `/openapi/v2/model/fashion-similarity` | POST | Text ↔ image cosine similarity scoring matrix | 1 credit |

## License

MIT
