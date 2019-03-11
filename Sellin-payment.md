---


---

<h1 id="sellin---compras-de-fornecedor-forma-de-pagamento">SellIn - Compras de Fornecedor (Forma de Pagamento)</h1>
<p>Modelo de Dados - Sellin-Payment</p>
<h3 id="forma-de-pagamento">Forma de Pagamento</h3>

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
<td>payment_method_id*</td>
<td>Identificador da Forma de Pagamento</td>
<td>string</td>
<td>–</td>
<td>–</td>
</tr>
<tr>
<td>method*</td>
<td>Método de Pagamento</td>
<td>string</td>
<td>–</td>
<td>“Boleto”</td>
</tr>
<tr>
<td>bin</td>
<td>BIN [6 Primeiros dígitos do cartão]</td>
<td>string</td>
<td>–</td>
<td>–</td>
</tr>
<tr>
<td>ccflag_id</td>
<td>Código da bandeira do cartão</td>
<td>string</td>
<td>tamanho máximo de 50 caracteres</td>
<td>“19389238”</td>
</tr>
<tr>
<td>condition*</td>
<td>Condição de pagamento</td>
<td>string</td>
<td>–</td>
<td>“Parcelado”</td>
</tr>
<tr>
<td>operation_id</td>
<td>Código da operação financeira</td>
<td>string</td>
<td>–</td>
<td>“92389328”</td>
</tr>
<tr>
<td>nsu</td>
<td>NSU</td>
<td>string</td>
<td>–</td>
<td>–</td>
</tr>
<tr>
<td>authorization</td>
<td>Autorização da transação</td>
<td>string</td>
<td>–</td>
<td>–</td>
</tr>
</tbody>
</table>
