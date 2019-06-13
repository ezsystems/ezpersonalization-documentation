# OXID

## Introduction

Your customers expect high-quality recommendations.
They want to be supported in their purchasing decision and selection process.
By using Yoochoose recommendations you increase the usability and the level of professionalism of your online shop.
The recommendations present products to the customers they had not expected to find - which distinguishes them from search.

If you are not familiar with the usage of recommendations, read the [introduction](../personalization/user_guide/introduction.md) and [use cases](../personalization/user_guide/use_cases.md) from the User Guide.
Otherwise you can proceed with the following steps.

## Requirements

OXID eShop version:

- CE &gt; 4.7.x
- EE, PE 5.x

## Network and firewall configuration

The OXID Recommendation module needs connection to the following endpoints:

- `admin.yoochoose.net`
- `reco.yoochoose.net`
- `event.yoochoose.net`

Both http (port 80) and https (port 443) ports must be open for outbound TCP connections.
You cannot build the firewall rule based on the IP addresses.
The Yoochoose infrastructure is located in the AWS cloud and IP addresses can be changed.

The OXID recommendation module loads recommendations using JavaScript after the shop page is already rendered.
If the Yoochoose infrastructure is not available, it won't affect the loading time of OXID webpages.

## Installation

Download the Yoochoose module package from the [Yoochoose Bitbucket repository](https://bitbucket.org/yoochoose/tracking).
Copy the content of the folder `src/plugins/oxid` into the modules folder of your OXID installation.

The structure should look like this:

    ./modules/yoochoose/yoochoose/..

Don't worry if you see a `yoochoose/yoochoose/` in the directory tree. This is correct.

If you have a subfolder `Mediaopt` inside the `modules` directory, remove it.
It is present in the older plugin versions.

## Activation

In the OXID administration back end go to `/Extentions/Modules/Yoochoose Recommendations` and click **Activate**.

![OXID activation](img/oxid_activate.png "OXID activation")

After that, refresh the browser window (or hit F5).
A new menu element `/Yoochoose` should appear under the menu Service.

## Registration

In the OXID administration back end go to `/Yoochoose/Config `and click **Register new Yoochoose account**.

![OXID registeration step 1](img/oxid_register.png "OXID registeration step 1")

Register an account 

![OXID registeration step 2](img/oxid_register2.png "OXID registeration step 2")

Ensure that OXID Connect is selected

![OXID Connect](img/oxid_connect.png "OXID Connect")

After successful registration process you will receive a customer ID and a license key by email.
Add this information into the corresponding fields in the module configuration page `/Yoochoose/Config`

![OXID configuration](img/oxid_config.png "OXID configuration")

Default recommendation settings are preconfigured and you can start tracking user data.

The customer ID and the license key can also be obtained later in the [YOOCHOOSE back end](https://admin.yoochoose.net).
Login with the email address you used in the registration process.

![OXID customer ID](img/oxid_customerid.png "OXID customer ID")

Please be patient. After the plugin is activated it takes about a day until the first recommendations are available.
The recommendation engine needs to collect statistical information before high quality recommendations can be provided.
If enough tracking data is available, they will be rendered in your shop.

## Structure and Functionality

The recommendation module is configured with default recommendation boxes throughout the OXID shop:

- Landing Page **Bestsellers** with most popular products
- Landing Page **Recommendations for You** recommendation based on your shopping taste

![Landing page 1](img/oxid_landing_page.png "Landing page 1")

- Category Page **Bestsellers** with the most popular products in the current category

![Current category](img/oxid_landing_page2.png "Current category")

- Product Detail Page **What other customers bought** with recommendations that others bought alongside the currently displayed product
- Product Detail Page **You may be interested in** with recommendations of alternative products that were often viewed together with the current one

![Detail Page](img/oxid_detail_page.png "Detail Page")

- Shopping Cart recommendations with products that fit your shopping basket

![Shopping Cart](img/oxid_shopping_cart.png "Shopping Cart")

## Disabling embedded recommendation

Several database-intensive cross selling boxes are available in OXID out of the box they should be deactivated.
It can be done in the OXID admin back end in `/Master Settings/Core Settings/Performance/Enhanced Performance Settings`

![Disabling embedded recommendation](img/oxid_disable_embedded.png "Disabling embedded recommendation")
