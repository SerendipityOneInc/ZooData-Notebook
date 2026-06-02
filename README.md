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
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SerendipityOneInc/APIClaw-Notebook/blob/main/e-commerce-search/product_search.ipynb) [Product Search](e-commerce-search/product_search.ipynb) | Find fashion products with natural-language queries. Covers brand, price, and retailer filtering. | `fashion-product-search` |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SerendipityOneInc/APIClaw-Notebook/blob/main/e-commerce-search/image_search.ipynb) [Image Search](e-commerce-search/image_search.ipynb) | Visual similarity search — upload an image, find matching products. Includes bounding-box cropping, text-guided search, and a "Shop the Look" pipeline. | `fashion-image-search` |

## API Reference

Full documentation: [apiclaw.io/api-docs](https://apiclaw.io/api-docs)

| Endpoint | Method | Description | Cost |
|----------|--------|-------------|------|
| `/openapi/v2/model/fashion-product-search` | POST | Text-based fashion product search across 200M+ items | 1 credit |
| `/openapi/v2/model/fashion-image-search` | POST | Visual similarity fashion product search | 1 credit |

## License

MIT
