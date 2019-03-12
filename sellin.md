---


---

<h1 id="sellin---compras-de-fornecedor">SellIn - Compras de Fornecedor</h1>
<p>Modelo de Dados - Sellin</p>
<h3 id="sellin---cabeçalho">SellIn - Cabeçalho</h3>

<table>
<thead>
<tr>
<th align="center">Campo</th>
<th align="center">Descrição</th>
<th align="center">tipo</th>
<th align="center">Restrições</th>
<th align="center">Exemplos</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">store_id*</td>
<td align="center">Identificador interno da loja</td>
<td align="center">integer ou string</td>
<td align="center">–</td>
<td align="center">1</td>
</tr>
<tr>
<td align="center">id*</td>
<td align="center">Identificador (NF) da compra</td>
<td align="center">string</td>
<td align="center">tamanho máximo de 50 caracteres</td>
<td align="center">“RCNTH345987”</td>
</tr>
<tr>
<td align="center">supplier_taxpayer_id*</td>
<td align="center">CNPJ do Fornecedor</td>
<td align="center">string</td>
<td align="center">tamanho máximo de 14 caracteres</td>
<td align="center">“14463765000172”</td>
</tr>
<tr>
<td align="center">sellin_timestamp*</td>
<td align="center">Data e hora da compra</td>
<td align="center">string</td>
<td align="center">satisfazer o padrão “YYYY-MM-DDTHH:MM:SS”</td>
<td align="center">“2017-08-20T14:55:08”</td>
</tr>
<tr>
<td align="center">nfe_access_key</td>
<td align="center">Chave de acesso para NFe/SAT</td>
<td align="center">string</td>
<td align="center">tamanho máximo de 50 caracteres</td>
<td align="center">“NFe31170901704848000164550020000018481058491134”</td>
</tr>
<tr>
<td align="center">other_expenses</td>
<td align="center">Outras despesas</td>
<td align="center">float</td>
<td align="center">–</td>
<td align="center">1.99</td>
</tr>
<tr>
<td align="center">seller_id</td>
<td align="center">CPF do vendedor associado a esta NF, caso exista vendedor relacionado</td>
<td align="center">string</td>
<td align="center">tamanho máximo de 11 caracteres</td>
<td align="center">“RCNTH345987”</td>
</tr>
<tr>
<td align="center">ipi</td>
<td align="center">Valor do IPI sobre a compra</td>
<td align="center">float</td>
<td align="center">–</td>
<td align="center">1.87</td>
</tr>
<tr>
<td align="center">iss</td>
<td align="center">Valor do ISS sobre a compra</td>
<td align="center">float</td>
<td align="center">–</td>
<td align="center">1.01</td>
</tr>
<tr>
<td align="center">sales_discount</td>
<td align="center">Valor de desconto na compra</td>
<td align="center">float</td>
<td align="center">–</td>
<td align="center">5.99</td>
</tr>
<tr>
<td align="center">insurance_price</td>
<td align="center">Valor do seguro</td>
<td align="center">float</td>
<td align="center">–</td>
<td align="center">2.0</td>
</tr>
<tr>
<td align="center">gross_total*</td>
<td align="center">Valor total da NF. Este valor deve vir com 4 casas decimais</td>
<td align="center">float</td>
<td align="center">–</td>
<td align="center">5.99</td>
</tr>
<tr>
<td align="center">cancellation_flag*</td>
<td align="center">Indica se esta compra foi cancelada ou não</td>
<td align="center">string</td>
<td align="center">Valores aceitos: “S” — para sim “N” — para não</td>
<td align="center">“S”</td>
</tr>
<tr>
<td align="center">nfe_series_number</td>
<td align="center">Número de Série da Nota Fiscal</td>
<td align="center">integer</td>
<td align="center">–</td>
<td align="center">1</td>
</tr>
<tr>
<td align="center">nfe_number</td>
<td align="center">Número da Nota Fiscal</td>
<td align="center">integer</td>
<td align="center">–</td>
<td align="center">1267232</td>
</tr>
<tr>
<td align="center">sales_addition</td>
<td align="center">Valor de acréscimo na compra</td>
<td align="center">float</td>
<td align="center">Este valor deve vir com 4 casas decimais</td>
<td align="center">4.55</td>
</tr>
<tr>
<td align="center">store_taxpayer_id*</td>
<td align="center">CNPJ da loja</td>
<td align="center">string</td>
<td align="center">tamanho máximo de 14 caracteres</td>
<td align="center">“14463765000100”</td>
</tr>
<tr>
<td align="center">net_total*</td>
<td align="center">Valor total da NF sem impostos e frete</td>
<td align="center">float</td>
<td align="center">Este valor deve vir com 4 casas decimais</td>
<td align="center">4.99</td>
</tr>
<tr>
<td align="center">freight_price</td>
<td align="center">Valor do frete</td>
<td align="center">float</td>
<td align="center">–</td>
<td align="center">1.0</td>
</tr>
<tr>
<td align="center">icms</td>
<td align="center">Valor do ICMS sobre a compra</td>
<td align="center">float</td>
<td align="center">–</td>
<td align="center">2.9</td>
</tr>
</tbody>
</table>
