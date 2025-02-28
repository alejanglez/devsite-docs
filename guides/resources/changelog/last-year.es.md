---
  indexable: false
---
# Release notes Mercado Pago 2019

Cada release note describe los cambios que aplican a una versión. Estos cambios pueden incluir:

- **Actualizaciones en APIs:** lanzamiento, modificación o eliminación de recursos, parámetros o campos en nuestras APIs.

- **Nuevos productos o funcionalidades:** Lanzamiento de herramientas que harán que puedas aceptar pagos de forma más fácil.

- **Anuncios:** Novedades relacionadas a alguno de nuestros productos o cambios a futuro.

- **Actualizaciones en la documentación:** Guías, referencias y tutoriales para ayudarte a monetizar tu negocio integrando Mercado Pago.

## 5 de Diciembre de 2019

En Mercado Pago buscamos siempre optimizar nuestra plataforma ofreciendo la más alta eficiencia y seguridad en el procesamiento de pagos.

En esta ocasión, estamos trabajando en el apagado de nuestra API de Checkout Custom versión 0 con el objetivo de mantener los más altos estándares de calidad.

Después del 12 de diciembre del 2019, la versión 0 dejara de tener soporte.

El apagado afecta a los siguientes recursos:

| Uso | Método | URI del Recurso deprecado |
| --- | --- | --- |
| Pago | `POST` | /checkout/custom/create_payment |
| Medio de Pagos | `GET` | /checkout/custom/payment_methods |
| Búsqueda de Medios de Pagos| `GET` | /checkout/custom/payment_methods/search |
| Emisores | `GET` | /checkout/custom/card_issuers |

En [este artículo](https://www.mercadopago.com.ar/developers/es/guides/online-payments/checkout-api/introduction) vas a encontrar los recursos equivalentes.

## 25 de Noviembre de 2019

Para cumplir con los más altos estándares de seguridad, buscamos siempre estar actualizados. Por eso, la versión antigua de **notificaciones IPN (Instant Payment Notification)** ya no estará disponible a partir del 9 de diciembre.

Si la estás usando, **tienes que revisar tu versión y actualizarla para evitar problemas y pérdidas de servicio.** En caso de no querer hacerlo, puedes usar otro tipo de notificaciones que ofrecemos.

Puedes encontrar toda la información necesaria en la [guía de la migración](https://www.mercadopago.com.ar/developers/es/guides/resources/changelog/migration-guides/ipn-ow-guide).

----[mlc, mco]----

## 25 de Septiembre de 2019

**Mejoras al flujo PSE, Webpay y Khipu.**

- Si se informa la url deseada en el campo “callback_url”, el usuario será redireccionado a dicha url luego de 15 segundos de realizado el pago.
- En caso de no informarse una “callback_url”, se muestra nuestra pantalla de confirmación, sin disparar la redirección.

------------
----[mlc]----

**Mejoras para pagos rechazados en Shopify**

- Se solucionó el problema cuando un cliente de Shopify selecciona débito como medio de pago vía Webpay, y navega hacia atrás en el browser, ya no se muestra la pantalla de confirmación, sino que se rechaza el pago.

------------

----[mlb, mlm, mlc, mco, mpe]----

## 29 de mayo de 2019

**Módulos oficiales con soporte de Mercado Pago**

Queremos darte la mejor experiencia, siempre. Por eso, te contamos cuáles son los módulos que cuentan con soporte oficial de Mercado Pago y que puedas tener un servicio personalizado cuando lo necesites:

------------
----[mla, mlu]----

## 29 de mayo de 2019

**Módulos oficiales con soporte de Mercado Pago**

Queremos darte la mejor experiencia, siempre. Por eso, te contamos cuáles son los módulos que cuentan con soporte oficial de Mercado Pago y que puedas tener un servicio personalizado cuando lo necesites:

------------


| Módulo | Versiones |
| --- | --- |
| WooCommerce | WordPress 3.1.x - 4.9.x, WooCommerce 2.6.x - 3.4.x |
| PrestaShop | Prestashop 1.6.x - 1.7.x |
| Magento | Community Edition 1.8.x - 1.9.x, Enterprise Edition 1.11.x - 1.14.x, Magento 2.0.0 - 2.3.x |
| Shopify | - |

[Ver módulos](https://www.mercadopago.com.ar/developers/es/guides/plugins).


----[mlb, mlm, mlc, mco, mpe]----

> Ten en cuenta que los módulos y plataformas no mencionadas solamente tienen soporte de la comunidad.

------------

----[mla, mlu]----

> Tené en cuenta que los módulos y plataformas no mencionadas solamente tienen soporte de la comunidad.

------------

----[mlb, mlm, mlc, mco, mpe]----

## 16 de abril de 2019

**Navegadores compatibles con Mercado Pago**

Actualizamos nuestros protocolos de seguridad para cumplir con los más altos estándares de seguridad.

Para seguir usando Mercado Pago sin problemas, es necesario que lo hagas desde las versiones soportadas por nuestros dominios:

------------


----[mla, mlu]----

## 16 de abril de 2019

**Navegadores compatibles con Mercado Pago**

Actualizamos nuestros protocolos de seguridad para cumplir con los más altos estándares de seguridad.

Para seguir usando Mercado Pago sin problemas, es necesario que lo hagas desde las versiones soportadas por nuestros dominios:

------------

| Navegador | Versión |
| --- | --- |
| Internet Explorer | 9 o posterior |
| Chrome | 6 o posterior |
| Android Browser | 2.3.3 o posterior |

----[mlb, mlm, mlc, mco, mpe]----
> Ten en cuenta que no vas a poder ingresar a ningún sitio de Mercado Pago con los navegadores no compatibles.
------------

----[mla, mlu]----
> Tené en cuenta que no vas a poder ingresar a ningún sitio de Mercado Pago con los navegadores no compatibles.
------------
