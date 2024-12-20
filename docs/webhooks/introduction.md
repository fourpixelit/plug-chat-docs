---
id: introduction
title: Introdução
---

## Conceituação

Neste tópico falaremos sobre os **RETORNOS** dos webhooks que utilizamos.

O Plug chat faz requisições com o método **POST** dos eventos realizados por ele para a URL configurada previamente. Para cada requisição há um corpo em JSON específico que será descrito em seguida.

:::caution Importante

Seu endpoint precisa aceitar um **POST**

Esses endpoints são para trocar a URL que a instância irá chamar quando o evento acontecer

:::

## O que é e para que serve?

Segundo o Google, Webhook é um recurso usado na internet para que uma aplicação se comunique com outra, fornecendo dados em tempo real sempre que um evento acontecer. Desta forma os dois sistemas realizam trocas de informações sem que nenhuma ação externa precise ser realizada.

Então se você está se integrando com o Plug e precisa receber informações pelo Whatsapp, é necessário prover estes end-points na sua aplicação para conseguirmos te avisar sobre tudo que acontece no seu Whatsapp. Ou seja, toda vez que o número conectado receber uma interação, vamos fazer uma requisição com o método POST para a URL configurada previamente. (Para cada requisição há um corpo em JSON específico)

---


:::tip Dica

- Não deixe de ler nossa sessão dicas, lá você vai encontrar alguns tópicos de como melhorar sua conexão com Plug e ter mais qualidade no serviço.

- Você não precisa configurar todos webhooks, mas quanto mais controle você possuir sobre sua instância mais vai conseguir extrair recursos e desenvolver negócios com Plug

:::

## Como configurar meu Webhook?

:::important

Nunca compartilhe o seu ID e token com ninguém.

:::
