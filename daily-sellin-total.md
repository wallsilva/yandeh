---


---

<h1 id="daily_sellin_total---valor-total-de-compra-por-dia">Daily_SellIn_Total - Valor total de compra por dia</h1>
<p>Modelo de Dados -  DAILY-SELLIN</p>
<h3 id="compra-total-por-dia">Compra total por dia</h3>

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
<td>date*</td>
<td>Data do dia</td>
<td>string</td>
<td>satisfazer o padrão “YYYY-MM-DD”</td>
<td>“2018-08-13”</td>
</tr>
<tr>
<td>type*</td>
<td>Indica qual o tipo de documento fiscal</td>
<td>string</td>
<td>limita-se apenas aos valores:“nfe”: Nota Fiscal Eletrônica</td>
<td>“nfe”</td>
</tr>
<tr>
<td>quantity*</td>
<td>Quantidade de documentos fiscais</td>
<td>integer</td>
<td>inteiro não-negativo</td>
<td>3759</td>
</tr>
<tr>
<td>amount*</td>
<td>Faturamento total</td>
<td>float</td>
<td>float não-negativo</td>
<td>123457.93</td>
</tr>
</tbody>
</table><h3 id="exemplo-em-sql">Exemplo em SQL:</h3>
<pre><code>SELECT store_id  AS "store_id", 
       date     AS "date", 
       type     AS "type", 
       quantity AS "quantity", 
       amount   AS "amount" 
FROM   view_dialy_sellin_total 
GROUP  BY date 
</code></pre>

