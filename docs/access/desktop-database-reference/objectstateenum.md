---
title: ObjectStateEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 48fcf6c0135b4704155aa23765e848de5b3e6313
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879953"
---
# <a name="objectstateenum"></a>ObjectStateEnum

**Aplica-se a**: Access 2013, o Office 2013

Especifica se um objeto está aberto ou fechado, conectando a uma fonte de dados, executando um comando ou recuperando dados.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adStateClosed</strong></p></td>
<td><p>0</p></td>
<td><p>Indica que o objeto está fechado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStateOpen</strong></p></td>
<td><p>1</p></td>
<td><p>Indica que o objeto está aberto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStateConnecting</strong></p></td>
<td><p>2</p></td>
<td><p>Indica que o objeto está conectando.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStateExecuting</strong></p></td>
<td><p>4</p></td>
<td><p>Indica que o objeto está executando um comando.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStateFetching</strong></p></td>
<td><p>8</p></td>
<td><p>Indica que as linhas do objeto estão sendo recuperadas.</p></td>
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
<td><p>AdoEnums.ObjectState.CLOSED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ObjectState.OPEN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ObjectState.CONNECTING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ObjectState.EXECUTING</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ObjectState.FETCHING</p></td>
</tr>
</tbody>
</table>

