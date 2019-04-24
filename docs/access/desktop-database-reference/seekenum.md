---
title: SeekEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f8334cbfc8e0f6a362a36e03984739d1d52b6f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314655"
---
# <a name="seekenum"></a>SeekEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica o tipo de [Seek](seek-method-ado.md) a ser executada.

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
<td><p>adSeekFirstEQ</p></td>
<td><p>1</p></td>
<td><p>Procura a primeira chave igual a <em>KeyValues</em>.</p></td>
</tr>
<tr class="even">
<td><p>adSeekLastEQ</p></td>
<td><p>duas</p></td>
<td><p>Procura a última chave igual a <em>KeyValues</em>.</p></td>
</tr>
<tr class="odd">
<td><p>adSeekAfterEQ</p></td>
<td><p>quatro</p></td>
<td><p>Procura uma chave igual a <em>KeyValues</em> ou apenas depois de onde essa correspondência ocorreu.</p></td>
</tr>
<tr class="even">
<td><p>adSeekAfter</p></td>
<td><p>8</p></td>
<td><p>Procura uma chave depois do local em que uma correspondência com <em>KeyValues</em> ocorreu.</p></td>
</tr>
<tr class="odd">
<td><p>adSeekBeforeEQ</p></td>
<td><p>dezesseis</p></td>
<td><p>Procura uma chave igual a <em>KeyValues</em> ou apenas antes do local em que essa correspondência ocorreu.</p></td>
</tr>
<tr class="even">
<td><p>adSeekBefore</p></td>
<td><p>32</p></td>
<td><p>Procura uma chave antes do local em que uma correspondência com <em>KeyValues</em> ocorreu.</p></td>
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
<td><p>AdoEnums. Seek. FIRSTEQ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Seek. LASTEQ</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Seek. AFTEREQ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Seek. AFTER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Seek. BEFOREEQ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Seek. BEFORE</p></td>
</tr>
</tbody>
</table>

