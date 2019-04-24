---
title: EditModeEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 246d9e29f084efb975783fd15c15993eba5a6e74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293578"
---
# <a name="editmodeenum"></a>EditModeEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica o status de edição de um registro.

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
<td><p><strong>adEditNone</strong></p></td>
<td><p>,0</p></td>
<td><p>Indica que nenhuma operação de edição está em andamento.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditInProgress</strong></p></td>
<td><p>1</p></td>
<td><p>Indica que os dados no registro atual foram modificados, mas não foram salvos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEditAdd</strong></p></td>
<td><p>duas</p></td>
<td><p>Indica que o método <a href="addnew-method-ado.md">AddNew</a> foi chamado e o registro atual no buffer de cópias é um novo registro que não foi salvo no banco de dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditDelete</strong></p></td>
<td><p>quatro</p></td>
<td><p>Indica que o registro atual foi excluído.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente do ADO/WFC

Pacote: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums. EditMode. NONE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EditMode. inPROGRESS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EditMode. ADD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EditMode. DELETE</p></td>
</tr>
</tbody>
</table>

