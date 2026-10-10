# Comparação Diária de Ações Automática (n8n)

Workflow no n8n que consulta diariamente ações de diferentes empresas por meio da API brapi, reúne as informações dos ativos, formata um resumo utilizando Java e envia o resultado por e-mail.

## Fluxo

```text
Disparo Automático → Organizar Tickers → Dividir Tickers → Loop → API brapi → Agregar Informações → Java → Enviar E-mail
```

| Nó | O que faz |
|---|---|
| **Schedule Trigger** | Inicia o fluxo automaticamente todos os dias |
| **Organizar Tickers** | Organiza a lista de códigos das ações que serão consultadas |
| **Dividir Tickers** | Separa os tickers para processamento |
| **Loop Over Items** | Percorre os tickers para consultar cada ação |
| **HTTP Request** | Consulta os dados das ações por meio da API brapi |
| **Aggregate** | Reúne as informações retornadas pelas consultas |
| **Java** | Formata e organiza os dados em uma mensagem estruturada |
| **Send Email** | Envia o resumo das ações por e-mail |

## Pré-requisitos

- Instância do n8n (cloud ou self-hosted)
- Acesso à API brapi
- Java para formatação das informações
- Credenciais de e-mail configuradas no n8n
- Lista de tickers das ações que serão monitoradas

Feito para praticar automações com n8n, integração com APIs, processamento de dados e envio automático de relatórios por e-mail.
