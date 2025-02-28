---
  indexable: false
---
# ZenCart - Mercado Pago Module (v1.5.x)

> WARNING
>
> Solo damos soporte a plugins oficiales
>
> Esta documentación no cuenta con soporte oficial de Mercado Pago. Si quieres realizar algún cambio, puedes [modificar el código abierto en GitHub](https://github.com/mercadopago/devsite-docs/blob/development/guides/plugins/unofficial/zencart.es.md).

## Funcionalidad

El módulo de Mercado Pago para ZenCart esta integrado con las siguientes funcionalidad y soluciones de pago:

* [Checkout básico (Redirect, Iframe ou Modal)](https://www.mercadopago.com.ar/developers/es/solutions/payments/basic-checkout/receive-payments/)
* Pagos con dos tarjetas

## Versión disponibles

| Versión del Plugin | Status | Versiones compatibles |
| --- | --- | --- |
| v1.0.1 | Stable (Current version) | ZenCart 1.5.x |

## Requisitos:

**PHP**

* PHP v5+
* Required extensions: MySQL, cURL

**Database**

* MySQL v5+

<a name="installation"></a>
## Instalación

1. Descargue el modulo de Mercado Pago.

2. Copia la carpeta del módulo en la raíz de tu tienda ZenCart.

## Configuración

1. En la página de administración de tu tienda, vaya hasta la opción **Modules > Payment**.

2. En **Payment Modules** seleccione **Mercado Pago**.

3. En **Mercado Pago** haga clic en el botón **Install**.

4. Ahora, es muy importante configurar las credenciales **CLIENT_ID** y **CLIENT_SECRET**.

  ![Setting client id and client secret](/images/zencart-credentials.png) <br />

Obtenga su [CLIENT_ID y CLIENT_SECRET]([FAKER][CREDENTIALS][URL]).

5. Configure el estado para IPN (Instant Payment Notification):

  ![Installation Instructions](/images/zencart-notification.png) <br />

  * **Choose the default status for a new order**: Setea el status de la orden cuando los pagos son aprobados.
  * **Choose the status of approved orders**: Setea el status de la orden cuando los pagos son aprobados.
  * **Choose the status when payment is pending**: Setea el status de la orden cuando los pagos son pendientes.
  * **Choose the status when payment is process**: Setea el status de la orden cuando los pagos están en proceso.
  * **Choose the status when payment was reject**: Setea el status de la orden cuando los pagos son rechazados.
  * **Choose the status of refunded orders**: Setea el status de la orden cuando los pagos son devueltos.
  * **Choose the status when client open a mediation**: Setea el status de la orden cuando los pagos están en mediación.
  * **Choose the status when payment was canceled**: Setea el status de la orden cuando los pagos son cancelados.

6. Otras configuraciones: <br/>

![Installation Instructions](/images/zencart-other_config_1.png) <br />

![Installation Instructions](/images/zencart-other_config_2.png) <br />

![Number of installments and other settings](/images/zencart-other_config_3.png) <br />

  * **Store Category**: Seleccione la categoría de la tienda;
  * **Redirect URL**: La  URL de redirección se genera automáticamente si está probando en un localhost no funcionará correctamente. Puedes cambiar la dirección a cualquier url de su preferencia;
  * **Enable Auto Return?**: Cuando esta opción está activada, al finalizar la compra el usuario es redirigido automáticamente a su tienda;
  * **Type Checkout**: Seleccione el tipo de checkout que se mostrará al comprador;
  * **Limit installments**: Seleccione el número de parcelas máximas que estará disponible para el comprador;
  * **Exclude Methods**: Seleccione los métodos de pago que desea **no aceptar**;
  * **Live or Sandbox**: Habilite el modo sandbox para realizar pagos de prueba;
  * **Sort order of display**: Orden de visualización de Mercado Pago;

## Soporte técnico

En el caso de que tenga alguna duda, problema o error tenemos un canal de contacto.
Contáctanos a nuestro canal de [soporte](/support) con la siguiente información:

* Email de su cuenta de Mercado Pago.
* Detalles sobre su duda, problema o error.
* Archivos que puedan ayudar en el entendimiento (Print-Screen, Video, Archivos de logs, etc).
* Versión del ZenCart.
* Versión del módulo, si está utilizando.
