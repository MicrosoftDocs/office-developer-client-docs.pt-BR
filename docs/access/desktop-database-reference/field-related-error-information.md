---
title: Informações sobre erros relacionados a campos
TOCTitle: Field-related error information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e853c45e4ee0de9a958ccc791bac3afcd305a23
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943560"
---
# <a name="field-related-error-information"></a>Informações sobre erros relacionados a campos


**Aplica-se a**: Access 2013, o Office 2013

Se um erro for diretamente relacionado a um campo (por exemplo, se os dados estiverem ausentes ou se o tipo for incorreto para o campo ), você poderá recuperar mais informações sobre a causa do problema examinando a propriedade **Status** do objeto **Field**. Essa propriedade foi aprimorada para fornecer informações específicas sobre o problema. Portanto, por exemplo, quando há falha em uma chamada de **UpdateBatch**, a causa do problema poderá ser determinada examinando-se a propriedade **Status** dos objetos **Field** em cada um dos registros afetados. A propriedade conterá um dos valores da constante **FieldStatusEnum**. A tabela a seguir inclui esses valores de particular interesse quando ocorre um erro.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFieldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>Indica que o campo não pode ser recuperado nem armazenado sem perda de dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6</p></td>
<td><p>Indica que os dados retornados do provedor sobrecarregaram o tipo de dados do campo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Indica que o valor padrão do campo foi usado durante a definição dos dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15</p></td>
<td><p>Indica que este campo foi ignorado durante a definição dos valores de dados na fonte. Nenhum valor foi definido pelo provedor.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>Indica que não é possível modificar o campo porque ele é uma entidade calculada ou derivada.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3</p></td>
<td><p>Indica que o provedor retornou um valor nulo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>Indica que o provedor não conseguiu obter espaço de repositório suficiente para concluir uma operação de movimentação ou cópia.</p></td>
</tr>
</tbody>
</table>

