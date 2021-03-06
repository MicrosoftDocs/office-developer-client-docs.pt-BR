---
title: LockTypeEnum (referência do banco de dados da área de trabalho do Access)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4b9dc49e647bdcd3123ade065da0c74538c9a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289861"
---
# <a name="locktypeenum"></a>LockTypeEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica o tipo de bloqueio colocado nos registros durante a edição.

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
<td><p><strong>adLockBatchOptimistic</strong></p></td>
<td><p>4 </p></td>
<td><p>Indica as atualizações em lote otimistas. Exigido para o modo de atualização em lote.</p></td>
</tr>
<tr class="even">
<td><p><strong>adLockOptimistic</strong></p></td>
<td><p>3 </p></td>
<td><p>Indica o bloqueio otimista, registro por registro. O provedor usa os registros de bloqueio otimistas apenas quando você chama o método <a href="update-method-ado.md">Update</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockPessimistic</strong></p></td>
<td><p>2 </p></td>
<td><p>Indica o bloqueio pessimista, registro por registro. O provedor faz o que for necessário para garantir a edição bem-sucedida dos registros, geralmente bloqueando os registros na fonte de dados imediatamente após a edição.</p></td>
</tr>
<tr class="even">
<td><p><strong>adLockReadOnly</strong></p></td>
<td><p>1 </p></td>
<td><p>Indica os registros somente leitura. Não é possível alterar os dados.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Não especifica um tipo de bloqueio. Para clones, o clone é criado com o mesmo tipo de bloqueio que o original.</p></td>
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
<td><p>AdoEnums.LockType.BATESTIMÍSTICA</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.LockType.OPTIMISTIC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.LockType.PESSIMISTIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.LockType.READONLY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.LockType.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

