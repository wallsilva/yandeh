---


---

<h1 id="sellin---compras-de-fornecedor-condição-de-pagamento">SellIn - Compras de Fornecedor (Condição de Pagamento)</h1>
<p>Modelo de Dados - Sellin - Installments</p>
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
<td>amount*</td>
<td>Valor da parcela</td>
<td>float</td>
<td>–</td>
<td>129.9</td>
</tr>
<tr>
<td>payment_term*</td>
<td>Prazo do pagamento da parcela em dias</td>
<td>integer</td>
<td>–</td>
<td>30</td>
</tr>
</tbody>
</table>
