---
  indexable: false
---
# Mercado Pago's release notes 2019

Each release note describes the new changes applying to a version. This changes may include:

- **API updates:** added, modified or deleted resources,parameters or fields in our APIs.

- **New products or features:** Launch of tools which will help you accept payments seamlessly.

- **Annoucements:** News related to any of our products or future changes.

- **Documentation updates:** Guides, references and tutorials to help you monetize your business by integrating Mercado Pago.

## December 5th, 2019

At Mercado Pago we always try to optimize our platform offering the highest efficiency and security in payment processing.

We are currently working on shutting down our Custom Checkout API version 0 in order to maintain the highest quality standards.

After December 12th, 2019 version 0 will stop having support.

The shutdown will involve the following resources:

| Use | Method | Deprecated resource URI |
| --- | --- | --- |
| Payment | `POST` | /checkout/custom/create_payment |
| Payment Methods | `GET` | /checkout/custom/payment_methods |
| Payment Methods search | `GET` | /checkout/custom/payment_methods/search |
| Card issuers | `GET` | /checkout/custom/card_issuers |

You can find the equivalent resources in [this article](https://www.mercadopago.com.ar/developers/en/guides/online-payments/checkout-api/introduction/).

## November 25, 2019

To meet the highest security standards, we seek to always be updated. Therefore, the old version of **IPN notifications (Instant Payment Notification)** will no longer be available from November 29.

If you are using it, **you must check your version and update it to avoid problems and loss of service.** In case you don't want to do it, you can use other types of notifications that we offer.

You can find all the necessary information in the [migration guide](https://www.mercadopago.com.br/developers/en/guides/resources/changelog/migration-guides/ipn-ow-guide). 

----[mlc, mco]----

## September 25th, 2019

**Flow improvements for PSE, Webpay y Khipu.**

- If customer “callback_url” is set for the payment, user is redirected to the defined url after 15 seconds.
- In case it is not defined, Mercado Pago´s success is displayed without redirection

------------
----[mlc]----

**Improvements for rejected payments in Webpay**

- Shopify: Problem solved when a client selects as payment method Debit in Webpay's flow. When the user tried to navigate backwards, the success receipt is no longer displayed, but the payment rejected screen is displayed.

------------

## May 29th, 2019

**Official modules with support from Mercado Pago**

We always want to give you the best experience. Therefore, we list the modules that have official support from Mercado Pago and that you can have personalized service as needed:

| Module | Versions |
| --- | --- |
| WooCommerce | WordPress 3.1.x - 4.9.x, WooCommerce 2.6.x - 3.4.x |
| PrestaShop | Prestashop 1.6.x - 1.7.x |
| Magento| Community Edition 1.8.x - 1.9.x, Enterprise Edition 1.11.x - 1.14.x, Magento 2.0.0 - 2.3.x |
| Shopify | - |

[View modules](https://www.mercadopago.com.ar/developers/en/guides/plugins).


> Please note that the modules and platforms not mentioned only have support from the community. 


## April 16th, 2019

**Browsers compatible with Mercado Pago**

We have updated our security protocols to meet the highest security standards.

To continue using Mercado Pago without problems, you must do it from the versions supported by our domains:


| Browser | Version |
| --- | --- |
| Internet Explorer | 9 or later |
| Chrome | 6 or later |
| Android Browser | 2.3.3 or later |


> Keep in mind that you will not be able to enter any Mercado Pago website using unsupported browsers.

