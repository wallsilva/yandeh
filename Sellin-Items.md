---


---

<h1 id="sellin---compras-de-fornecedor-itens">SellIn - Compras de Fornecedor (Itens)</h1>
<p>Modelo de Dados - Sellin-Items</p>
<h3 id="sellin---itens">SellIn - Itens</h3>

<table>
<thead>
<tr>
<th>Campo</th>
<th>Descrição</th>
<th>Tipo</th>
<th>Restrições</th>
<th>Exemplo</th>
</tr>
</thead>
<tbody>
<tr>
<td>store_id*</td>
<td>Identificador interno da loja</td>
<td>integer ou string</td>
<td>–</td>
<td>1</td>
</tr>
<tr>
<td>sellin_timestamp*</td>
<td>Data e hora da compra</td>
<td>string</td>
<td>satisfazer o padrão “YYYY-MM-DDTHH:MM:SS”</td>
<td>“2017-08-20T14:55:08”</td>
</tr>
<tr>
<td>id*</td>
<td>Identificador (NF) da compra</td>
<td>string</td>
<td>tamanho máximo de 50 caracteres</td>
<td>“RCNTH345987”</td>
</tr>
<tr>
<td>code*</td>
<td>Código interno do produto vendido</td>
<td>string</td>
<td>tamanho máximo de 30 caracteres</td>
<td>“COCA300”</td>
</tr>
<tr>
<td>isbn</td>
<td>ISBN</td>
<td>string</td>
<td>Tamanho mínimo de 10 caracteres e máximo de 13 caracteres</td>
<td>–</td>
</tr>
<tr>
<td>description*</td>
<td>Descrição do produto</td>
<td>string</td>
<td>tamanho máximo de 50 caracteres</td>
<td>“Castanha portuguesa”</td>
</tr>
<tr>
<td>ean*</td>
<td>Código de barras do produto, se houver. Este campo aceita tanto EAN-13 quanto DUN-14</td>
<td>string</td>
<td>tamanho máximo de 14 caracteres</td>
<td>“7891149201006”</td>
</tr>
<tr>
<td>addition</td>
<td>Valor de acréscimo total neste item</td>
<td>float</td>
<td>Este valor deve ser enviado com 4 casas. decimais</td>
<td>34.5698</td>
</tr>
<tr>
<td>discount</td>
<td>Valor de desconto total neste item</td>
<td>float</td>
<td>Este valor deve ser enviado com 4 casas. decimais</td>
<td>34.5698</td>
</tr>
<tr>
<td>net_total*</td>
<td>Valor total das unidades vendidas, sem impostos e frete</td>
<td>float</td>
<td>Este valor deve ser enviado com 4 casas. decimais</td>
<td>56.9805</td>
</tr>
<tr>
<td>measurement_unit</td>
<td>Unidade de medida</td>
<td>string</td>
<td>–</td>
<td>“UN”</td>
</tr>
<tr>
<td>gross_total*</td>
<td>Valor total das unidades vendidas, sem desconto ou acréscimo</td>
<td>float</td>
<td>Este valor deve ser enviado com 4 casas. decimais</td>
<td>56.98</td>
</tr>
<tr>
<td>unit_value*</td>
<td>Valor unitário do produto, sem desconto ou acréscimo</td>
<td>float</td>
<td>Este valor deve ser enviado com 4 casas. decimais</td>
<td>45.98</td>
</tr>
<tr>
<td>quantity*</td>
<td>Quantidade do produto</td>
<td>float</td>
<td>Este valor deve ser enviado com 4 casas. decimais</td>
<td>1.0000</td>
</tr>
<tr>
<td>manufacturer_code</td>
<td>Código do fabricante</td>
<td>string</td>
<td>–</td>
<td>8928329</td>
</tr>
</tbody>
</table>
