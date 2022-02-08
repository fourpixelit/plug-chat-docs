---
id: status
title: Status da instância
---

## Método

#### /Status

`GET` https://www.plugchat.com.br/api/whatsapp/status

---

## Conceituação

Este método é responsável por lhe passar informações sobre a saúde da sua instância no Plug, para uma boa qualidade de envio e recebimento é preciso tomar os seguinte cuidados:

- Configure os webhooks no Plug para receber notificações sobre mudanças no status da sua instância.

- Desabilite a otimização de bateria do celular conectado mesmo que seja um emulador (exemplo para Android https://youtu.be/Z1baLLXyvTM).

- Monitore os atributos deste método.

---

## Atributos

| Atributos | Tipo | Descrição |
| :-- | :-: | :-- |
| connected | boolean | Indica se seu número está conectado ao Plug |
| session | boolean | Indica se sua instância tem um token ativo no WhatsApp |
| error | string | Informa detalhes caso algum dos atributos não esteja true - 'You are already connected.' - 'You need to restore the session.' - 'You are not connected.' |
| smartphoneConnected | boolean | Indica se o celular está conectado à internet |

---

## Code

<iframe src="//api.apiembed.com/?source=https://raw.githubusercontent.com/Z-API/z-api-docs/main/json-examples/status.json&targets=all" frameborder="0" scrolling="no" width="100%" height="500px" seamless></iframe>
