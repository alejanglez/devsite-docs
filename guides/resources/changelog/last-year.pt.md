---
  indexable: false
---
# Release notes Mercado Pago 2019

Cada release note descreve as alterações que se aplicam a uma versão. Essas alterações podem incluir:

- **Atualizações em APIs:** lançamentos, modificações ou eliminação de recursos, parâmetros ou campos em nossas APIs.

- **Novos produtos ou funcionalidades:** Lançamentos de ferramentas que farão com que possa aceitar pagamentos de forma mais fácil.

- **Anúncios:** Novidades relacionadas a algum de nossos produtos ou alterações futuras.

- **Atualizações na documentação:** Guias, referências e tutoriais para te ajudar a monetizar seu negócio integrando Mercado Pago.

## 5 de dezembro de 2019

No Mercado Pago, sempre buscamos otimizar nossa plataforma, oferecendo a mais alta eficiência e segurança no processamento de pagamentos.

Nesta ocasião, estamos trabalhando na descontinuação da versão 0 da API do Checkout Custom para manter os mais altos padrões de qualidade.

Após 12 de dezembro de 2019, a versão 0 não será mais suportada.

O desligamento afetará os seguintes recursos:

| Serviço | Método | URI do Recurso depreciado |
| --- | --- | --- |
| Pagamento | `POST` | /checkout/custom/create_payment |
| Meio de Pagamento | `GET` | /checkout/custom/payment_methods |
| Busca de Meios de Pagamentos| `GET` | /checkout/custom/payment_methods/search |
| Emissores | `GET` | /checkout/custom/card_issuers |

[Neste link](https://www.mercadopago.com.br/developers/pt/guides/online-payments/checkout-api/introduction), você encontrará os recursos que vão substituir os que estão sendo depreciados.

## 24 de novembro de 2019

Para atender aos mais altos padrões de segurança, buscamos estar sempre atualizados. Portanto, a versão antiga das **notificações IPN (Notificação de pagamento instantâneo)** não estará mais disponível a partir do dia 9 de dezembro.

Se a estiver usando, **você deve revisar sua versão e atualizá-la para evitar problemas e perda de serviço.** Caso você não queira fazer isso, pode usar outro tipo de notificação que oferecemos. 

Confira todas as informações necessárias no [manual da migração](https://www.mercadopago.com.br/developers/pt/guides/resources/changelog/migration-guides/ipn-ow-guide).

----[mlc, mco]----

## 25 de Setembro de 2019

**Melhorias no fluxo PSE, Webpay e Khipu.**

- Se a URL desejada for informada no campo “callback_url”, o usuário será redirecionado a respectiva url 15 segundos após realização do pagamento.
- Caso um “callback_url” não seja informado, nossa tela de confirmação será exibida, sem acionar o redirecionamento.

------------
----[mlc]----

**Melhorias para pagamentos recusados no Shopify**

- Houve a solução do problema que ocorria quando um cliente do Shopify selecionava débito como meio de pagamento via Webpay e voltava ao navegador, a tela de confirmação não é mais exibida, mas sim o pagamento é rejeitado.

------------

## 29 de maio de 2019

**Módulos oficiais com suporte do Mercado Pago**

Queremos dar a melhor experiência para você sempre. Por isso, informamos quais módulos contam com suporte oficial do Mercado Pago e que você pode contar com serviço personalizado sempre que precisar:  

| Módulo | Versões |
| --- | --- |
| WooCommerce | WordPress 3.1.x - 4.9.x, WooCommerce 2.6.x - 3.4.x |
| PrestaShop | Prestashop 1.6.x - 1.7.x |
| Magento | Community Edition 1.8.x - 1.9.x, Enterprise Edition 1.11.x - 1.14.x, Magento 2.0.0 - 2.3.x |
| Shopify | - |

[Ver módulos](https://www.mercadopago.com.ar/developers/pt/guides/plugins).

> Lembre-se de que os módulos e plataformas não mencionados têm suporte apenas da comunidade. 


## 16 de abril de 2019

**Navegadores compatíveis com o Mercado Pago**

Atualizamos nossos protocolos de segurança para atender os mais altos padrões de segurança.

Para continuar usando o Mercado Pago sem problemas, é necessário que você o faça usando as versões suportadas pelos nossos domínios:


| Navegador | Versão |
| --- | --- |
| Internet Explorer | 9 ou posterior |
| Chrome | 6 ou posterior |
| Android Browser | 2.3.3 ou posterior |


> Lembre-se de que você não poderá acessar nenhum site do Mercado Pago com os navegadores incompatíveis.

