# APIClaw Notebooks

Interactive Colab notebooks demonstrating [APIClaw](https://apiclaw.io) APIs — e-commerce intelligence and AI model endpoints.

## Getting Started

1. Get a free API key (1,000 credits) at [apiclaw.io/register](https://apiclaw.io/register)
2. Click any **Open in Colab** badge below
3. Paste your API key when prompted

## Notebooks

### E-Commerce

| Notebook | Description | APIs Used |
|----------|-------------|-----------|
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SerendipityOneInc/APIClaw-Notebook/blob/main/e-commerce/fashion_product_search_demo.ipynb) [Text Search](e-commerce/fashion_product_search_demo.ipynb) | Find fashion products with natural-language queries. Covers brand, price, and retailer filtering. | `fashion-product-search` |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SerendipityOneInc/APIClaw-Notebook/blob/main/e-commerce/fashion_image_search_demo.ipynb) [Image Search](e-commerce/fashion_image_search_demo.ipynb) | Visual similarity search — upload an image, find matching products. Includes bounding-box cropping, text-guided search, and a "Shop the Look" pipeline. | `fashion-image-search` |

## API Reference

Full documentation: [apiclaw.io/api-docs](https://apiclaw.io/api-docs)

| Endpoint | Method | Description | Cost |
|----------|--------|-------------|------|
| `/openapi/v2/model/fashion-product-search` | POST | Text-based fashion product search across 200M+ items | 1 credit |
| `/openapi/v2/model/fashion-image-search` | POST | Visual similarity fashion product search | 1 credit |

## License

MIT
