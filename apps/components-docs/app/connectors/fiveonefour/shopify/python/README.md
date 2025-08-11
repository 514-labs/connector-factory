# Python Shopify Connector

A production-ready, read-only Python connector for Shopify that adheres to our [API Connector Specification](../api-connector.mdx). This connector provides a standardized interface for extracting data from Shopify stores with built-in resilience, rate limiting, and pagination.

## 🚀 Quick Start

```python
from shopify_connector import ShopifyConnector

# Initialize and connect
connector = ShopifyConnector({
    "shop": "your-store.myshopify.com",
    "apiVersion": "2024-07",
    "accessToken": "your-admin-api-token"
})

connector.connect()

# Extract data
products = connector.get('/products')
orders = connector.paginate('/orders')

connector.disconnect()
```

## 📚 Documentation

- **[Documentation Index](docs.md)** - Navigate to the information you need
- **[Getting Started](getting-started.md)** - Setup your Shopify store and configure the connector
- **[Architecture](architecture.md)** - Technical implementation details and API mapping
- **[Configuration](configuration.md)** - Configuration options and examples
- **[Testing](testing.md)** - Testing strategy and examples
- **[Why GraphQL?](why-graphql.md)** - Our implementation approach and rationale

## ✨ Features

- **Read-only data extraction** for Products, Orders, Customers, Inventory, and more
- **Automatic pagination** via Shopify's Link headers
- **Built-in resilience** with retries, rate limiting, and circuit breaking
- **Standardized interface** compliant with our API connector specification
- **GraphQL under the hood** for better performance and future-proofing
- **Incremental extraction** support with bookmark management

## 🔧 Requirements

- Python 3.8+
- Shopify store with Admin API access
- Custom app with appropriate read scopes

## 📦 Installation

```bash
pip install shopify-connector
```

## 🎯 Use Cases

- **Data pipelines** and ETL processes
- **Analytics** and reporting
- **Data synchronization** between systems
- **Backup** and archival operations

## 🔗 Resources

- [Shopify Admin API Documentation](https://shopify.dev/api/admin)
- [API Connector Specification](../api-connector.mdx)
- [Getting Started Guide](getting-started.md)

## 🤝 Contributing

This connector follows our standard patterns. See the [Architecture](architecture.md) document for implementation details and the [Testing](testing.md) guide for development practices.


