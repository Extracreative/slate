# Products #

The products API allows you to create, view, update, and delete individual, or a batch, of products.

## Product properties ##

| Attribute               | Type      | Description                                                                                                          |
|-------------------------|-----------|----------------------------------------------------------------------------------------------------------------------|
| `id`                    | integer   | Unique identifier for the resource. <i class="label label-info">read-only</i>                                        |
| `name`                  | string    | Product name.                                                                                                        |
| `slug`                  | string    | Product slug.                                                                                                        |
| `permalink`             | string    | Product URL. <i class="label label-info">read-only</i>                                                               |
| `date_created`          | date-time | The date the product was created, in the site's timezone. <i class="label label-info">read-only</i>                  |
| `date_created_gmt`      | date-time | The date the product was created, as GMT. <i class="label label-info">read-only</i>                                  |
| `date_modified`         | date-time | The date the product was last modified, in the site's timezone. <i class="label label-info">read-only</i>            |
| `date_modified_gmt`     | date-time | The date the product was last modified, as GMT. <i class="label label-info">read-only</i>                            |
| `type`                  | string    | Product type. Options: `simple`, `grouped`, `external` and `variable`. Default is `simple`.                          |
| `status`                | string    | Product status (post status). Options: `draft`, `pending`, `private` and `publish`. Default is `publish`.            |
| `featured`              | boolean   | Featured product. Default is `false`.                                                                                |
| `catalog_visibility`    | string    | Catalog visibility. Options: `visible`, `catalog`, `search` and `hidden`. Default is `visible`.                      |
| `description`           | string    | Product description.                                                                                                 |
| `short_description`     | string    | Product short description.                                                                                           |
| `sku`                   | string    | Unique identifier.                                                                                                   |
| `price`                 | string    | Current product price. <i class="label label-info">read-only</i>                                                     |
| `regular_price`         | string    | Product regular price.                                                                                               |
| `sale_price`            | string    | Product sale price.                                                                                                  |
| `date_on_sale_from`     | date-time | Start date of sale price, in the site's timezone.                                                                    |
| `date_on_sale_from_gmt` | date-time | Start date of sale price, as GMT.                                                                                    |
| `date_on_sale_to`       | date-time | End date of sale price, in the site's timezone.                                                                      |
| `date_on_sale_to_gmt`   | date-time | End date of sale price, as GMT.                                                                                      |
| `price_html`            | string    | Price formatted in HTML. <i class="label label-info">read-only</i>                                                   |
| `on_sale`               | boolean   | Shows if the product is on sale. <i class="label label-info">read-only</i>                                           |
| `purchasable`           | boolean   | Shows if the product can be bought. <i class="label label-info">read-only</i>                                        |
| `total_sales`           | integer   | Amount of sales. <i class="label label-info">read-only</i>                                                           |
| `virtual`               | boolean   | If the product is virtual. Default is `false`.                                                                       |
| `downloadable`          | boolean   | If the product is downloadable. Default is `false`.                                                                  |
| `downloads`             | array     | List of downloadable files. See [Product - Downloads properties](#product-downloads-properties)                      |
| `download_limit`        | integer   | Number of times downloadable files can be downloaded after purchase. Default is `-1`.                                |
| `download_expiry`       | integer   | Number of days until access to downloadable files expires. Default is `-1`.                                          |
| `external_url`          | string    | Product external URL. Only for external products.                                                                    |
| `button_text`           | string    | Product external button text. Only for external products.                                                            |
| `tax_status`            | string    | Tax status. Options: `taxable`, `shipping` and `none`. Default is `taxable`.                                         |
| `tax_class`             | string    | Tax class.                                                                                                           |
| `manage_stock`          | boolean   | Stock management at product level. Default is `false`.                                                               |
| `stock_quantity`        | integer   | Stock quantity.                                                                                                      |
| `stock_status`          | string    | Controls the stock status of the product. Options: `instock`, `outofstock`, `onbackorder`. Default is `instock`.     |
| `backorders`            | string    | If managing stock, this controls if backorders are allowed. Options: `no`, `notify` and `yes`. Default is `no`.      |
| `backorders_allowed`    | boolean   | Shows if backorders are allowed. <i class="label label-info">read-only</i>                                           |
| `backordered`           | boolean   | Shows if the product is on backordered. <i class="label label-info">read-only</i>                                    |
| `sold_individually`     | boolean   | Allow one item to be bought in a single order. Default is `false`.                                                   |
| `weight`                | string    | Product weight.                                                                                                      |
| `dimensions`            | object    | Product dimensions. See [Product - Dimensions properties](#product-dimensions-properties)                            |
| `shipping_required`     | boolean   | Shows if the product need to be shipped. <i class="label label-info">read-only</i>                                   |
| `shipping_taxable`      | boolean   | Shows whether or not the product shipping is taxable. <i class="label label-info">read-only</i>                      |
| `shipping_class`        | string    | Shipping class slug.                                                                                                 |
| `shipping_class_id`     | integer   | Shipping class ID. <i class="label label-info">read-only</i>                                                         |
| `reviews_allowed`       | boolean   | Allow reviews. Default is `true`.                                                                                    |
| `average_rating`        | string    | Reviews average rating. <i class="label label-info">read-only</i>                                                    |
| `rating_count`          | integer   | Amount of reviews that the product have. <i class="label label-info">read-only</i>                                   |
| `related_ids`           | array     | List of related products IDs. <i class="label label-info">read-only</i>                                              |
| `upsell_ids`            | array     | List of up-sell products IDs.                                                                                        |
| `cross_sell_ids`        | array     | List of cross-sell products IDs.                                                                                     |
| `parent_id`             | integer   | Product parent ID.                                                                                                   |
| `purchase_note`         | string    | Optional note to send the customer after purchase.                                                                   |
| `categories`            | array     | List of categories. See [Product - Categories properties](#product-categories-properties)                            |
| `tags`                  | array     | List of tags. See [Product - Tags properties](#product-tags-properties)                                              |
| `images`                | array     | List of images. See [Product - Images properties](#product-images-properties)                                        |
| `attributes`            | array     | List of attributes. See [Product - Attributes properties](#product-attributes-properties)                            |
| `default_attributes`    | array     | Defaults variation attributes. See [Product - Default attributes properties](#product-default-attributes-properties) |
| `variations`            | array     | List of variations IDs. <i class="label label-info">read-only</i>                                                    |
| `grouped_products`      | array     | List of grouped products ID.                                                                                         |
| `menu_order`            | integer   | Menu order, used to custom sort products.                                                                            |
| `meta_data`             | array     | Meta data. See [Product - Meta data properties](#product-meta-data-properties)                                       |

                                  

## Create a product ##

This API helps you to add a new product.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-post">POST</i>
		<h6>/v1/products</h6>
	</div>
</div>

> Example of how to create a `simple` product:

```shell
curl -X POST https://metadataplus.com/v1/products \
	-u consumer_key:consumer_secret \
	-H "Content-Type: application/json" \
	-d '{
  "name": "Premium Quality",
  "type": "simple",
  "regular_price": "21.99",
  "description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
  "short_description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
  "categories": [
    {
      "id": 9
    },
    {
      "id": 14
    }
  ],
  "images": [
    {
      "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_front.jpg"
    },
    {
      "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_back.jpg"
    }
  ]
}'
```

> JSON response example:

```json
{
}
```

## Retrieve a product ##

This API lets you retrieve and view a specific product by ID.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/v1/products/&lt;id&gt;</h6>
	</div>
</div>

```shell
curl https://metadataplus.com/v1/products/794 \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
{
}
```

## List all products ##

This API helps you to view all the products.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/v1/products</h6>
	</div>
</div>

```shell
curl https://metadataplus.com/v1/products \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
{
}
```

#### Available parameters ####

| Parameter        | Type    | Description                                                                                                                             |
|------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `context`        | string  | Scope under which the request is made; determines fields present in response. Options: `view` and `edit`. Default is `view`.            |
| `page`           | integer | Current page of the collection. Default is `1`.                                                                                         |
| `per_page`       | integer | Maximum number of items to be returned in result set. Default is `10`.                                                                  |
| `search`         | string  | Limit results to those matching a string.                                                                                               |
| `after`          | string  | Limit response to resources published after a given ISO8601 compliant date.                                                             |
| `before`         | string  | Limit response to resources published before a given ISO8601 compliant date.                                                            |
| `exclude`        | array   | Ensure result set excludes specific IDs.                                                                                                |
| `include`        | array   | Limit result set to specific ids.                                                                                                       |
| `offset`         | integer | Offset the result set by a specific number of items.                                                                                    |
| `order`          | string  | Order sort attribute ascending or descending. Options: `asc` and `desc`. Default is `desc`.                                             |
| `orderby`        | string  | Sort collection by object attribute. Options: `date`, `id`, `include`, `title`, `slug`, `price`, `popularity` and `rating`. Default is `date`.                           |
| `parent`         | array   | Limit result set to those of particular parent IDs.                                                                                     |
| `parent_exclude` | array   | Limit result set to all items except those of a particular parent ID.                                                                   |
| `slug`           | string  | Limit result set to products with a specific slug.                                                                                      |
| `status`         | string  | Limit result set to products assigned a specific status. Options: `any`, `draft`, `pending`, `private` and `publish`. Default is `any`. |
| `type`           | string  | Limit result set to products assigned a specific type. Options: `simple`, `grouped`, `external` and `variable`.                         |
| `sku`            | string  | Limit result set to products with a specific SKU.                                                                                       |
| `featured`       | boolean | Limit result set to featured products.                                                                                                  |
| `category`       | string  | Limit result set to products assigned a specific category ID.                                                                           |
| `tag`            | string  | Limit result set to products assigned a specific tag ID.                                                                                |
| `shipping_class` | string  | Limit result set to products assigned a specific shipping class ID.                                                                     |
| `attribute`      | string  | Limit result set to products with a specific attribute.                                                                                 |
| `attribute_term` | string  | Limit result set to products with a specific attribute term ID (required an assigned attribute).                                        |
| `tax_class`      | string  | Limit result set to products with a specific tax class. Default options: `standard`, `reduced-rate` and `zero-rate`.                    |
| `on_sale`        | boolean | Limit result set to products on sale.                                                                                                   |
| `min_price`      | string  | Limit result set to products based on a minimum price.                                                                                  |
| `max_price`      | string  | Limit result set to products based on a maximum price.                                                                                  |
| `stock_status`   | string  | Limit result set to products with specified stock status. Options: `instock`, `outofstock` and `onbackorder`.                           |

## Update a product ##

This API lets you make changes to a product.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-put">PUT</i>
		<h6>/v1/products/&lt;id&gt;</h6>
	</div>
</div>

```shell
curl -X PUT https://metadataplus.com/v1/products/794 \
	-u consumer_key:consumer_secret \
	-H "Content-Type: application/json" \
	-d '{
  "regular_price": "24.54"
}'
```

> JSON response example:

```json
{
}
```

## Delete a product ##

This API helps you delete a product.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-delete">DELETE</i>
		<h6>/v1/products/&lt;id&gt;</h6>
	</div>
</div>

```shell
curl -X DELETE https://metadataplus.com/v1/products/794?force=true \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
{
}
```

## Batch update products ##

This API helps you to batch create, update and delete multiple products.

<aside class="notice">
Note: By default it's limited to up to 100 objects to be created, updated or deleted. 
</aside>

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-post">POST</i>
		<h6>/v1/products/batch</h6>
	</div>
</div>

```shell
curl -X POST https://metadataplus.com/v1/products/batch \
	-u consumer_key:consumer_secret \
	-H "Content-Type: application/json" \
	-d '{
  "create": [
    {
      "name": "Woo Single #1",
      "type": "simple",
      "regular_price": "21.99",
      "virtual": true,
      "downloadable": true,
      "downloads": [
        {
          "name": "Woo Single",
          "file": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/cd_4_angle.jpg"
        }
      ],
      "categories": [
        {
          "id": 11
        },
        {
          "id": 13
        }
      ],
      "images": [
        {
          "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/cd_4_angle.jpg"
        }
      ]
    },
    {
      "name": "New Premium Quality",
      "type": "simple",
      "regular_price": "21.99",
      "description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
      "short_description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
      "categories": [
        {
          "id": 9
        },
        {
          "id": 14
        }
      ],
      "images": [
        {
          "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_front.jpg"
        },
        {
          "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_back.jpg"
        }
      ]
    }
  ],
  "update": [
    {
      "id": 799,
      "default_attributes": [
        {
          "id": 6,
          "name": "Color",
          "option": "Green"
        },
        {
          "id": 0,
          "name": "Size",
          "option": "M"
        }
      ]
    }
  ],
  "delete": [
    794
  ]
}'
```

> JSON response example:

```json
{
}
```
