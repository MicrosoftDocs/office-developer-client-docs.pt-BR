---
title: FilterGroupEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 5c42b703536e931405325d3a91219a148e6580d1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873282"
---
# <a name="filtergroupenum"></a>FilterGroupEnum

**Aplica-se a**: Access 2013, o Office 2013

Especifica o grupo de registros a serem filtrados a partir de um [Recordset](recordset-object-ado.md).

<br/>

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
<td><p><strong>adFilterAffectedRecords</strong></p></td>
<td><p>2</p></td>
<td><p>Filtros para visualizar apenas os registros afetados pela última chamada <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a> ou <a href="cancelbatch-method-ado.md">CancelBatch</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterConflictingRecords</strong></p></td>
<td><p>5</p></td>
<td><p>Filtra para visualizar os registros que falharam na última atualização em lote.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterFetchedRecords</strong></p></td>
<td><p>3</p></td>
<td><p>Filtra para visualizar os registros na memória cache atual — ou seja, os resultados da última chamada para recuperar os registros do banco de dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterNone</strong></p></td>
<td><p>0</p></td>
<td><p>Remove o filtro atual e restaura todos os registros para visualização.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterPendingRecords</strong></p></td>
<td><p>1</p></td>
<td><p>Filtra para visualizar apenas os registros que foram alterados, mas que ainda não foram enviados ao servidor. Aplicável apenas para o modo de atualização em lote.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Pacote: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.FilterGroup.AFFECTEDRECORDS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FilterGroup.CONFLICTINGRECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FilterGroup.FETCHEDRECORDS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FilterGroup.NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FilterGroup.PENDINGRECORDS</p></td>
</tr>
</tbody>
</table>

