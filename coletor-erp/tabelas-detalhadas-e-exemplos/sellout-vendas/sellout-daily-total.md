---
description: Modelo de Dados - "Daily_Sellout_Total" | Valor total de venda por dia
---

# Sellout - Daily Total

### Vendas total por dia

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :--- | :--- | :--- | :--- | :--- |
| store\_id\* | Identificador interno da loja | integer ou string | -- | 1 |
| date\* | Data do dia | string | satisfazer o padrão “YYYY-MM-DD” | “2018-08-13” |
| type\* | Indica qual o tipo de documento fiscal | string | limita-se apenas aos valores:“nfe”: Nota Fiscal Eletrônica | “nfe” |
| quantity\* | Quantidade de documentos fiscais | integer | inteiro não-negativo | 3759 |
| amount\* | Faturamento total | float | float não-negativo | 123457.93 |

#### Exemplo da consulta em SQL:

```text
    SELECT store_id AS "store_id", 
           date     AS "date", 
           type     AS "type", 
           quantity AS "quantity", 
           amount   AS "amount" 
    FROM   view_daily_sellout_total 
    GROUP  BY date 
```

