# Magento2

## Introduction

If you are not familiar with the usage of recommendations, please read at least the [first](../personalization/user_guide/introduction.md) [two](../personalization/user_guide/use_cases.md) pages of the User Guide.

## Installation

First of all you need to install the Yoochoose Recommendation Engine Extension. It can be done through the [https://marketplace.magento.com](https://marketplace.magento.com/) webpage (search for "yoochoose"). The extension is free to download and install. The service itself is based on performance of the recommendations. See our pricing page <http://www.yoochoose.com/en/pricing/> for details.

In order to install the extension on your local Magento2 installation, your purchases need to be in sync via the Web Wizard Setup -&gt; Component Manager (<http://devdocs.magento.com/guides/v2.1/comp-mgr/module-man/compman-start.html>)

## Account Registration

Before the recommendation engine can be enabled for your web shop, you must register a new "Magento Connect" account on the Yoochoose web page.

[http://www.yoochoose.com/en/pricing](http://www.yoochoose.com/en/pricing/) 

Select the Magento Module in the option box (Magento2 and Magento use the same registration link).

![](img/magento_register.png)

or use the direct link <https://admin.yoochoose.net/login.html?product=magento_Direct&lang=en_US#login>.

An account contains a default scenario configuration for a standard web shop. If you are configuring a highly visited web shop (over a million page requests per month), it makes sense to ask for special consulting and phone support by Yoochoose GmbH.

The registration itself is straightforward and self explaining. After it is finished, you will get a customer ID and the license key for the recommendation extension.

## Activation of the YOOCHOOSE Extension in the Magento2 Backend

The Extension configuration/enabling is located in the Magento Admin Panel under Stores → Configuration → YOOCHOOSE

![](img/magento_activate.png)

In the admin interface of Magento 2 you can now enter the Customer ID and License Key information that you obtained after the successful registration process.

## Firewall Configuration

The Magento2 Recommendation module needs connection to the Yoochoose configuration server: `admin.yoochoose.net`

Both http (port 80) and https (port 443) ports must be open for outbound TCP connections. You cannot build the firewall rule based on IP. The Yoochoose infrastructure is located in the AWS cloud and the IP addresses can change.

## Available Recommendation Blocks

The Yoochoose extension works automatically after the installation and begins to track page visitors. Following blocks are available for recommendations:

- Bestseller are shown on the home page for all visitors and on the main category pages. 
- Personal recommendations are shown to registered customers or to anonymous visitors with a persistent or long living session. It analyses the purchasing and click history of the visitors and suggests new products.
- Related products are products that customers usually buy together with the current product (for example, butter together with bread).
- Up-Selling recommendations (on the product details block) show products that customers buy instead of the current product (for example printer "Canon" instead of "HP").
- Cross selling products are similar to the related products, but they are calculated based on the customer's shopping cart.

![](img/magento_landing_page.png "Landing and Category page")

![](img/magento_detail_page.png "Detail Page")

![](img/magento_shopping_cart.png "Shopping Cart")

## Personalized Search integration

We also offer a Personalized Search Service which can search for Vendors, Category and Products. It can be activated in the Magento2 back end in the Extension configuration.

![](img/magento_personalized_search.png)

An example of the search results can be seen here:

![](img/magento_search_results.png)

## Development and Maintenance

Further development of the extension is welcome. We have a bitbucket repository located under [https://bitbucket.org/yoochoose](https://bitbucket.org/yoochoose/). Don't hesitate to contact us for improvements, bug fixes or anything else related to the extension.
