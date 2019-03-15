---
description: Modelo de Dados - "SellOut" | Vendas para Clientes
---

# Sellout \(Vendas\)

| A entidade Sellout  tem como registros cada uma das vendas realizadas para os clientes. Estando preparada para descrever cada um dos seguintes tipos fiscais: ECF, CF-e, NF-e e NFC-e. |
| :--- |


## SellOut <a id="sellin---itens"></a>

<table>
  <thead>
    <tr>
      <th style="text-align:left">Campo</th>
      <th style="text-align:left">Descri&#xE7;&#xE3;o</th>
      <th style="text-align:left">Tipo</th>
      <th style="text-align:left">Restri&#xE7;&#xF5;es</th>
      <th style="text-align:left">Exemplo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">store_id*</td>
      <td style="text-align:left">Identificador interno da loja</td>
      <td style="text-align:left">integer ou string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">1</td>
    </tr>
    <tr>
      <td style="text-align:left">id*</td>
      <td style="text-align:left">Identificador da venda</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">tamanho m&#xE1;ximo de 50 caracteres</td>
      <td style="text-align:left">&#x201C;RCNTH345987&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">sellout_timestamp*</td>
      <td style="text-align:left">Data e hora da venda</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">satisfazer o padr&#xE3;o &#x201C;YYYY-MM-DDTHH:MM:SS&#x201D;</td>
      <td style="text-align:left">&#x201C;2017-08-20T14:55:08&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">nome_operador</td>
      <td style="text-align:left">Nome do operador do PDV</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">&#x201C;Maria Cristina&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">nome_vendedor</td>
      <td style="text-align:left">Nome do vendedor</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">&#x201C;Ana Maria&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">store_taxpayer_id*</td>
      <td style="text-align:left">CNPJ da loja que realizou a venda</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">tamanho exato de 14 caracteres</td>
      <td style="text-align:left">&#x201C;05345647000122&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">buyer_taxpayer_id</td>
      <td style="text-align:left">CPF ou CNPJ do comprador final</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">tamanho exato de 11 ou 14 caracteres</td>
      <td style="text-align:left">&#x201C;83230677323&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">checkout_id</td>
      <td style="text-align:left">Identificador do ponto de venda</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">&#x201C;2938923&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">receipt_number</td>
      <td style="text-align:left">N&#xFA;mero do documento fiscal (NF-e/NFC-e/CF-e)</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">tamanho m&#xE1;ximo de 50 caracteres</td>
      <td style="text-align:left">&#x201C;33093&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">receipt_series_number</td>
      <td style="text-align:left">S&#xE9;rie do documento fiscal (NF-e/NFC-e/CF-e) ou CCF (ECF)</td>
      <td
      style="text-align:left">string</td>
        <td style="text-align:left">No caso de documento ECF, obrigat&#xF3;rio informar o CCF neste campo</td>
        <td
        style="text-align:left">&#x201C;27&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">coo</td>
      <td style="text-align:left">N&#xFA;mero do COO (ECF)</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Campo obrigat&#xF3;rio para documentos tipo ECF</td>
      <td style="text-align:left">&#x201C;123742&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">nfe_access_key</td>
      <td style="text-align:left">Chave do documento NFC-e/CF-e associado &#xE0; venda</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Satisfazer o padr&#xE3;o exato de come&#xE7;ar com 3 caracteres de tipo
        (&#x201C;NFe&#x201D; ou &#x201C;CFe&#x201D;) seguido por 44 caracteres
        num&#xE9;ricos</td>
      <td style="text-align:left">
        <p>NFCe:&#x201C;NFe31170901704848000164650020000018481058491134&#x201D; ou</p>
        <p>CF-e: &#x201C;CFe35150310860014000139590010000162181020002180&#x201D;;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">device_id</td>
      <td style="text-align:left">N&#xFA;mero do dispositivo</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p></p>
        <p>Deve sempre ser fornecido para documentos do tipo ECF e em forma completa
          (em vez de reduzida). <b>Tamanho m&#xE1;ximo de 50 caracteres</b>
        </p>
      </td>
      <td style="text-align:left">&#x201C;BE1000199329329922&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">seller_id</td>
      <td style="text-align:left">CPF do vendedor associado a esta, caso exista vendedor relacionado</td>
      <td
      style="text-align:left">string</td>
        <td style="text-align:left">tamanho exato de 11 caracteres</td>
        <td style="text-align:left">&#x201C;83230677323&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">sales_addition*</td>
      <td style="text-align:left">Valor de acr&#xE9;scimo na venda</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">0.50</td>
    </tr>
    <tr>
      <td style="text-align:left">sales_discount*</td>
      <td style="text-align:left">Valor de desconto na venda</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">1.75</td>
    </tr>
    <tr>
      <td style="text-align:left">subtotal*</td>
      <td style="text-align:left">Valor do subtotal da venda</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">5.93</td>
    </tr>
    <tr>
      <td style="text-align:left">cancellation_flag*</td>
      <td style="text-align:left">Indica se a venda foi cancelada ou n&#xE3;o</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>limita-se apenas aos valores:</p>
        <p>&#x25CF; &#x201C;N&#x201D; : venda n&#xE3;o-cancelada &#x25CF; &#x201C;S&#x201D;
          : venda cancelada</p>
      </td>
      <td style="text-align:left">&#x201C;N&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">operation</td>
      <td style="text-align:left">Tipo da opera&#xE7;&#xE3;o realizada</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>limita-se apenas aos valores:</p>
        <p>&#x25CF; &#x201C;E&#x201D; : entrada</p>
        <p>&#x25CF; &#x201C;S&#x201D; : sa&#xED;da</p>
        <p>&#x25CF; &#x201C;DE&#x201D; : devolu&#xE7;&#xE3;o de entrada</p>
        <p>&#x25CF; &#x201C;DS&#x201D; : devolu&#xE7;&#xE3;o de sa&#xED;da</p>
        <p>&#x25CF; &#x201C;N&#x201D; : neutro</p>
        <p>&#x25CF; &#x201C;NULL&#x201D; : n&#xE3;o dispon&#xED;vel</p>
      </td>
      <td style="text-align:left">&#x201C;E&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">transaction_type</td>
      <td style="text-align:left">Indica qual tipo de transa&#xE7;&#xE3;o realizada</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>limita-se apenas aos valores:</p>
        <p>&#x25CF; &#x201C;J&#x201D; : ajuste de estoque</p>
        <p>&#x25CF; &#x201C;P&#x201D; : faturamento de pedido</p>
        <p>&#x25CF; &#x201C;S&#x201D; : normal</p>
        <p>&#x25CF; &#x201C;E&#x201D; : entrada</p>
        <p>&#x25CF; &#x201C;D&#x201D; : transfer&#xEA;ncia entre dep&#xF3;sitos</p>
        <p>&#x25CF; &#x201C;T&#x201D; : transfer&#xEA;ncia</p>
      </td>
      <td style="text-align:left">&quot;P&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">ipi</td>
      <td style="text-align:left">Valor do IPI sobre a venda</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">1.87</td>
    </tr>
    <tr>
      <td style="text-align:left">iss</td>
      <td style="text-align:left">Valor do ISS sobre a venda</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">1.01</td>
    </tr>
    <tr>
      <td style="text-align:left">frete</td>
      <td style="text-align:left">Valor de frete da venda</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">25.98</td>
    </tr>
    <tr>
      <td style="text-align:left">tipo</td>
      <td style="text-align:left">Indica qual tipo de documento fiscal</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>limita-se apenas aos valores:</p>
        <p>&#x25CF; &#x201C;ecf&#x201D; : SPED Fiscal</p>
        <p>&#x25CF; &#x201C;nfce&#x201D; : Nota Fiscal de Consumidor Eletr&#xF4;nica</p>
        <p>&#x25CF; &#x201C;sat&#x201D; : SAT Fiscal</p>
        <p>&#x25CF; &#x201C;nfe&#x201D; : Nota Fiscal Eletr&#xF4;nica</p>
      </td>
      <td style="text-align:left">&#x201C;nfce&#x201D;</td>
    </tr>
  </tbody>
</table>

#### Exemplo da consulta em SQL:

```text
SELECT store_id              AS "store_id", 
       sellout_timestamp     AS "sellout_timestamp", 
       id                    AS "id", 
       nome_operador         AS "nome_operador", 
       nome_vendedor         AS "nome_vendedor", 
       store_taxpayer_id     AS "store_taxpayer_id", 
       buyer_taxpayer_id     AS "buyer_taxpayer_id", 
       checkout_id           AS "checkout_id", 
       receipt_number        AS "receipt_number", 
       receipt_series_number AS "receipt_series_number", 
       coo                   AS "coo", 
       nfe_access_key        AS "nfe_access_key", 
       device_id             AS "device_id", 
       seller_id             AS "seller_id", 
       sales_addition        AS "sales_addition", 
       sales_discount        AS "sales_discount", 
       subtotal              AS "subtotal", 
       cancellaion_flag      AS "cancellaion_flag", 
       operation             AS "operation", 
       transaction_type      AS "transaction_type", 
       ipi                   AS "ipi", 
       iss                   AS "iss", 
       frete                 AS "frete", 
       tipo                  AS "tipo" 
FROM   view_sellout  
```

