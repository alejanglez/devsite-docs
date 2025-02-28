# Magento 2

## Requirements to integrate

| Requirement | Description |
| --- | --- |
| Magento Version | 2.x |
| Environment | LAMP (Linux, Apache, MySQL, and PHP)<br/>LNMP stack |
| Operational System | Linux x86-64 |
| Memory requirement | Minimum 2GB of RAM |
| Web Server | Apache 2.x<br/>Nginx 1.7.x |
| PHP Versions | 5.6.x<br/>7.0.2<br/>7.0.6–7.0.x<br/> |
| MySQL Version | MySQL 5.6<br/>MariaDB and Percona are compatible with Magento because we support MySQL 5.6 APIs. |
| Extension Dependencies | bc-math (Magento Commerce only)<br/>curl<br/>gd, ImageMagick 6.3.7 (or later) or both<br/>intl<br/>bstring<br/>mcrypt<br/>hash<br/>openssl<br/>PDO/MySQL<br/>SimpleXML<br/>soap<br/>xml<br/>xsl<br/>zip<br/> |
| PHP 7 only | json<br/>iconv |
| SSL | It is a requirement that you have an SSL certificate.<br/>During testing in Sandbox you will be able to run at http. |


## Features

The module of Mercado Pago to Magento is integrated with the features and payment solutions:

* [Basic Checkout (Checkout Pro)](https://www.mercadopago.com.br/developers/en/guides/online-payments/checkout-pro/introduction/)
    * [Split payments (Two cards)](https://www.mercadopago.com.br/developers/en/guides/online-payments/checkout-pro/configurations/#bookmark_payments_with_two_credit_cards)
    * [Refunds of Payments](https://www.mercadopago.com.br/developers/en/guides/manage-account/account/cancellations-and-refunds/)


* Custom Checkout
    * [Payment with Credit Card](https://www.mercadopago.com.br/developers/en/guides/online-payments/checkout-api/receiving-payment-by-card/)
    * [One Click Pay (Customers and Cards)](https://www.mercadopago.com.br/developers/en//guides/online-payments/checkout-api/advanced-integration/)
    * [Paid with other payment methods](https://www.mercadopago.com.br/developers/en/guides/online-payments/checkout-api/other-payment-ways/)
    * [Refunds of Payments](https://www.mercadopago.com.br/developers/en/guides/manage-account/account/cancellations-and-refunds)


* Other features
    * Customizable success page


## Installation

    This process will explain the installation of the Mercado Pago module via Composer:

**Installation via Composer**

1) Currently available two versions of modules, where each of them will provide a type of checkout:

* If you want to process payments with **Checkout Redirect**, you will need to install version 2.x of the Mercado Pago module. To install this version run the command:

> composer require mercadopago/magento2-plugin:2.*

* If you want to process payments with **Custom Checkout** with Credit Card or Ticket, use version 3.x of the module. This version is optimized for this type of checkout. To install this version run the command:

> composer require mercadopago/magento2-plugin:3.*

2) Then update magento with new modules:

> bin/magento setup:upgrade

3) Execute the command to clean the Magento cache:

> bin/magento cache:clean

4) When the store is in **productive** mode, it is necessary to generate the static files again:

> bin/magento setup:static-content:deploy

5) If you have problems with folder permission when accessing the store, you must renew the permissions:

> chmod 777 -R var/ pub/ generated/

6) Very Good! The module of Mercado Pago was successfully installed.


## Credit Card and Ticket Configuration (Custom Checkout)

This process will explain how to configure the module to accept payments with Checkout Custom with Credit Card and Tickets:

1) Go to **Stores > Configuration > Sales > Payment Methods**.

2) To set up the credentials go to Mercado Pago > Credentials, you will see the field Public Key and Access Token. Get your credentials in [the Credentials section]([FAKER][CREDENTIALS][URL]).

> There are two types of credentials:
> * Trial credentials: The credentials in this way are used for testing.
> * Productive credentials: The credentials in this way are used to receive payments in production. To use the credentials of the production mode you must activate your credentials.

3) With your credentials filled, you need to enable payment methods. Go to **Custom Checkout - Credit And Debit Card**, click in **Configure** and check **Enable** as **Yes**. Make this process for **Custom Checkout - Offline Payments Methods (Ticket)** too and then click on **Save Config**.

![Mercado Pago Custom Checkout Configuration](images/magento2/mercadopago_custom_checkout_configuration.png)

4) Very good! The Checkout Custom with Credit Card and Ticket has been configured and enabled successfully!


## Basic Checkout Configuration

This process will explain how to configure the module to accept payments with Basic Checkout in Redirect, Iframe or Lightbox:

1) Go to **Stores > Configuration > Sales > Payment Methods**.

2) To set up the credentials go to Mercado Pago - Classic Checkout, click in Configure. you will see the field Client id and Client Secret. Get your credentials in the [Credentials section]([FAKER][CREDENTIALS][URL]).

3) With your credentials filled, you need to enable payment methods. Click in **Configure** and check **Enable** as **Yes**. Configure the **Type Checkout** and if the user must return to your store at the end of the checkout (**Auto Redirect**).

![Checkout Pro Redirect Configuration](images/magento2/mercadopago_global_configuration.png)

4) Very good! The Basic Checkout with Credit Card and Ticket has been configured and enable successfully!


## Payment Notification status settings

This process will explain how to set up order statuses for payment notifications:

1) Go to **Stores > Configuration > Sales > Payment Methods**.

2) To configure the statuses go to **Mercado Pago - Global Configuration**, go to the option **Order Status Options**.
For each payment status you can choose an order status, as soon as your store receives the payment notification the module will automatically update the order to the chosen status. To save the settings click the **Save Config** button.

> The module is prepared to receive payment notifications automatically, that is, without the need to configure your Mercado Pago account or module.

3) Very Good! The notification statuses have been successfully configured.
