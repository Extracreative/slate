# Introduction #

**Metadata Plus Backend API Documentation**

Metadata API is enriched product data. The service uses data extraction and human and AI input to enhance product data. 

The API is organized around REST. All requests should be made over SSL. All request and response bodies, including errors, are encoded in JSON.

We also have some specific language bindings to make integration easier. You can switch the programming language of the examples with the tabs in the top right.

Currently we support the following official client:

* shell: cURL
* javascript: Node.js
* php: PHP
* python: Python

The following table shows API Metadata versions:

| API Version |
|-------------|
| `v1`        |

## Requirements ##

To use the latest version of the REST API you must be using:

* You may access the API over either HTTPS.


## Official libraries ##

- [JavaScript](https://www.npmjs.com/package/@woocommerce/woocommerce-rest-api) Library
- [PHP](https://packagist.org/packages/automattic/woocommerce) Library
- [Python](https://pypi.python.org/pypi/WooCommerce) Library

```javascript
// Install:
// npm install --save @woocommerce/woocommerce-rest-api

// Setup:
const WooCommerceRestApi = require("@woocommerce/woocommerce-rest-api").default;
// import WooCommerceRestApi from "@woocommerce/woocommerce-rest-api"; // Supports ESM

const WooCommerce = new WooCommerceRestApi({
  url: 'http://example.com', // Your store URL
  consumerKey: 'consumer_key', // Your consumer key
  consumerSecret: 'consumer_secret', // Your consumer secret
  version: 'wc/v3' // WooCommerce WP REST API version
});
```

```php
<?php
// Install:
// composer require automattic/woocommerce

// Setup:
require __DIR__ . '/vendor/autoload.php';

use Automattic\WooCommerce\Client;

$woocommerce = new Client(
    'http://example.com', // Your store URL
    'consumer_key', // Your consumer key
    'consumer_secret', // Your consumer secret
    [
        'wp_api' => true, // Enable the WP REST API integration
        'version' => 'wc/v3' // WooCommerce WP REST API version
    ]
);
?>
```

```python
# Install:
# pip install woocommerce

# Setup:
from woocommerce import API

wcapi = API(
    url="http://example.com", # Your store URL
    consumer_key="consumer_key", # Your consumer key
    consumer_secret="consumer_secret", # Your consumer secret
    wp_api=True, # Enable the WP REST API integration
    version="wc/v3" # WooCommerce WP REST API version
)
```

<aside class="notice">
	Use the tabs in the top-right corner of this page to see how to install and use each library.
</aside>

