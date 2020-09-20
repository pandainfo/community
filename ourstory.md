# Our story

## Main requirements

An independent bookstore in Vienna wants to run a FLOSS webshop
with particular requirements.
There are special needs for book sellers in Austria, Germany and
Switzerland.
To run a modern webshop, support for ONIX for books (XML) is needed
to get the catalogue data, and for EDIFACT/EANCOM to automatically
order books and exchange invoices etc. with the distributors.

## Key specifications

So, our bookstore basically needs

* a webshop (self-hosted; cloud hosting optional)
* based on modern coding standards and easy to extend
* using PHP Composer dependency manager for plugins and themes
* including exclusively FLOSS modules and themes (with Free Software / "Open Source" licenses like GPL, AGPL, or MIT-style such as Apache 2.0 etc.)
* with EDI connection for B2B book orders upon delivery with different book distributions (KNO/KNV, Prolit, MOHR MORAWA, etc.)
* with ONIX XML import for new products
* replacing SKU / article no. by ISBN / EAN
* with SumUp connection for payment
* with CRM functionality for GDPR compliant customer contact
* with newsletter management for marketing campaigns and event invitations
* with optional connection to an ERP and to a cash register system or financial accounting system.

What is missing — apart from a nice theme, testing and integration of all components — was the development of the ONIX and EDI connectors.

## ONIX module

The requirements for the ONIX module include

* daily updates checking for new articles, stock number, prize changes, etc.
* storing product data in a proper database
* querying of catalogue data and inventory data when ordering in the webshop
* telling customers whether a product is on stock in the bookstore or not

## EDIFACT module

The requirements for the EDI module include

* Automatic data exchange for orders via EDI interface
* Implementation of the following EDI message types
  * DESADV for shipping notifications
  * INVOIC for invoice data
  * ORDERS for order data
  * ORDRSP for order confirmations
* Provision of electronic delivery bills via INVOIC message
* Integration of a common EDI library for [PHP](https://packagist.org/package/search?query=EDIFACT) or [JS](https://www.npmjs.com/search?q=EDIFACT) (for parser & generator) could make things easier
  * [PHP tools to process EDI messages in UN/EDIFACT format](https://github.com/php-edifact/edifact)

A sample message for ORDERS looks like this

```xml
UNH+0073400004+ORDERS:D:96A:UN:EAN008'BGM+220+0073400004+9'DTM+137:20200821:102'NAD+BY+9007981311232::9'NAD+SU+14914::86'
LIN+1++4014489122555:EN'QTY+21:1'FTX+LIN++DUY:1B'FTX+LIN++OWN:1B'RFF+ON:200891'RFF+CR:200891'
LIN+2++9783451068522:EN'QTY+21:1'FTX+LIN++DUY:1B'FTX+LIN++OWN:1B'RFF+ON:201120'RFF+CR:201120'
LIN+3++9783579077888:EN'QTY+21:1'FTX+LIN++DUY:1B'FTX+LIN++OWN:1B'RFF+ON:200890'RFF+CR:200890'
LIN+4++9783770459339:EN'QTY+21:1'FTX+LIN++DUY:1B'FTX+LIN++OWN:1B'RFF+ON:201107'RFF+CR:201107'
LIN+5++9783770702398:EN'QTY+21:1'FTX+LIN++DUY:1B'FTX+LIN++OWN:1B'RFF+ON:201059'RFF+CR:201059'
LIN+6++9783789113819:EN'QTY+21:1'FTX+LIN++DUY:1B'FTX+LIN++OWN:1B'RFF+ON:201054'RFF+CR:201054'
LIN+7++9783791501451:EN'QTY+21:1'FTX+LIN++DUY:1B'FTX+LIN++OWN:1B'RFF+ON:201055'RFF+CR:201055'
LIN+8++9783839226704:EN'QTY+21:1'FTX+LIN++DUY:1B'FTX+LIN++OWN:1B'RFF+ON:201116'RFF+CR:201116'
LIN+9++9783895615368:EN'QTY+21:1'FTX+LIN++DUY:1B'FTX+LIN++OWN:1B'RFF+ON:201072'RFF+CR:201072'
LIN+10++9783942581899:EN'QTY+21:1'FTX+LIN++DUY:1B'FTX+LIN++OWN:1B'RFF+ON:201149'RFF+CR:201149'
LIN+11++9783964435118:EN'QTY+21:1'FTX+LIN++DUY:1B'FTX+LIN++OWN:1B'RFF+ON:201083'RFF+CR:201083'
LIN+12++9783990820131:EN'QTY+21:1'FTX+LIN++DUY:1B'FTX+LIN++OWN:1B'RFF+ON:201086'RFF+CR:201086'
LIN+13++9783990820544:EN'QTY+21:1'FTX+LIN++DUY:1B'FTX+LIN++OWN:1B'RFF+ON:201085'RFF+CR:201085'
UNS+S'UNT+85+0073400004'
```

## Further features

Additional plugins include

* WP Hardening by Astra Security
* WooCommerce Subscriptions
* fork of [WooCommerce Multilingual](https://github.com/wp-premium/woocommerce-multilingual) on a public git repo for use with PHP composer
* [WooCommerce Admin Dashboard](https://wordpress.org/plugins/woocommerce-admin/)
* adoption of WooCommerce EU VAT Number
* adoption of Advanced Custom Fields Pro (ACF)

## Project goals

The defined project goals of the bookstore are as follows.

1. Via the webshop it is shown whether a title
   1. is in stock in the bookstore (the stock needs to be manually entered when creating/registering the article in the webshop or ERP) or
   2. is in stock on delivery (automatically querying the webshop's product database in real time)
2. If a title is ordered from the bookstore's stock, the bookstore receives an email
3. If a title is not in stock in the bookstore, the order is automatically forwarded to the delivery department
4. The bookstore receives shipping notifications and delivery notes or invoices via EDI (see above)
