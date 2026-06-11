---
id: send-message-text
title: Enviar texto simples
---

## Método

#### /send-text

`POST` https://www.plugchat.com.br/api/whatsapp/send-text

## Header

#### Toda requisição http feita precisa passar sua header de autorização.

|      Key       |        Value        |
| :------------: | :-----------------: |
| Authorization: | 1nEFbU3EktLnV7LIIzX |

---

## Conceituação

Neste método você poderá enviar textos simples mas, você pode incrementá-los utilizando a formatação de texto e emojis, por exemplo. Caso você ainda não saiba como fazer isso, clique nos links abaixo e siga as instruções:

- Para saber como formata fontes no Whatsapp [clique aqui]

- Você também pode utilizar **quebra linhas** em suas mensagens porém isso pode ser feito de formas diferentes, isso muda por fatores como a plataforma que sua aplicação esta rodando e linguagem de programação utilizada, até o momento indentificamos as seguinte:

  > - \n
  > - \r
  > - \r\n
  > - %0a

  Verifique a que mais se adequa ao seu caso.

  **Se descobrir uma maneira nova de fazer quebra de linhas por favor nos avise :)**

- Outro recurso que você pode explorar é a utilização de emojis, se você precisar pegar alguns emojis use este [link]

[clique aqui]: https://faq.whatsapp.com/general/chats/how-to-format-your-messages/?lang=pt_br
[link]: https://fsymbols.com/pt/emoji/

:::tip Sobre emojis

Sobre emojis o que você precisa saber é que ele é um caracter ASCII normal assim com existe a fonte Times New Roman por exemplo, existem fontes de emojis, pense que você pode criar sua própria >galeria de emojis.

Para fazer o teste basta copiar um emoji e colar em seu texto! Você pode utilizar este aqui 🤪 se quiser.

:::

---

## Atributos

### Obrigatórios

| Atributos | Tipo | Descrição |
| :-- | :-: | :-- |
| phone | string | Telefone (ou ID do grupo para casos de envio para grupos) do destinatário no formato DDI DDD NUMERO Ex: 551199999999. **IMPORTANTE** Envie somente números, sem formatação ou máscara |
| message | string | Texto a ser enviado |

### Opcionais

| Atributos | Tipo | Descrição |
| :-- | :-: | :-- |
| messageId | String | Atributo utilizado para responder uma mensagem do chat, basta adicionar o messageId da mensagem que queira responder neste atributo |
| delayMessage | number | Nesse atributo um delay é adicionado na mensagem. Você pode decidir entre um range de 1~15 sec, significa quantos segundos ele vai esperar para enviar a próxima mensagem. (Ex "delayMessage": 5, ). O delay default caso não seja informado é de 1~3 sec |

---

## Request Body

```json
{
  "phone": "5511999999999",
  "message": "Welcome to *Plug Chat*"
}
```

---

## Response

### 200

| Atributos | Tipo   | Descrição      |
| :-------- | :----- | :------------- |
| zaapId    | string | id no plug     |
| messageId | string | id no whatsapp |

Exemplo

```json
{
  "zaapId": "3999984263738042930CD6ECDE9VDWSA",
  "messageId": "D241XXXX732339502B68"
}
```

### 405

Neste caso certifique-se de que está enviando corretamente a especificação do método, ou seja, verifique se você enviou o POST ou GET conforme especificado no início deste tópico.

### 415

Caso você receba um erro 415, certifique de adicionar na headers da requisição o "Content-Type" do objeto que você está enviando, em sua grande maioria "application/json"

---

## Code

<iframe src="//api.apiembed.com/?source=https://raw.githubusercontent.com/fourpixelit/plug-chat-docs/main/json-examples/send-text.json&targets=all" frameborder="0" scrolling="no" width="100%" height="500px" seamless></iframe>
