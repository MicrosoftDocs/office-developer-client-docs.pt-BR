---
title: IsolationLevelEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: cb8873a7ddfc62429847b561736df4bfa91d429d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872841"
---
# <a name="isolationlevelenum"></a>IsolationLevelEnum

**Aplica-se a**: Access 2013, o Office 2013

Especifica o nível de isolamento da transação para um objeto [Connection](connection-object-ado.md).

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
<td><p><strong>adXactUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Indica que o provedor está usando um nível de isolamento diferente do especificado, mas que o nível não pode ser determinado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactChaos</strong></p></td>
<td><p>16</p></td>
<td><p>Indica que as alterações pendentes de transações mais altamente isoladas não podem ser sobregravadas.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactBrowse</strong></p></td>
<td><p>256</p></td>
<td><p>Indica que a partir de uma transação você pode visualizar as alterações sem compromisso em outras transações.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactReadUncommitted</strong></p></td>
<td><p>256</p></td>
<td><p>O mesmo que <strong>adXactBrowse</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactCursorStability</strong></p></td>
<td><p>4096</p></td>
<td><p>Indica que a partir de uma transação você pode visualizar as alterações em outras transações apenas depois que forem confirmadas.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactReadCommitted</strong></p></td>
<td><p>4096</p></td>
<td><p>O mesmo que <strong>adXactCursorStability</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactRepeatableRead</strong></p></td>
<td><p>65536</p></td>
<td><p>Indica que a partir de uma transação você não pode ver as alterações feitas em outras transações, mas que a repetição da consulta pode recuperar novos objetos <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactIsolated</strong></p></td>
<td><p>1048576</p></td>
<td><p>Indica que as transações são conduzidas no isolamento de outras transações.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactSerializable</strong></p></td>
<td><p>1048576</p></td>
<td><p>O mesmo que <strong>adXactIsolated</strong>.</p></td>
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
<td><p>AdoEnums.IsolationLevel.UNSPECIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.IsolationLevel.CHAOS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.BROWSE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.IsolationLevel.READUNCOMMITTED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.CURSORSTABILITY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.IsolationLevel.READCOMMITTED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.REPEATABLEREAD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.IsolationLevel.ISOLATED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.SERIALIZABLE</p></td>
</tr>
</tbody>
</table>

