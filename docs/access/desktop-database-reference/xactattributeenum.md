---
title: XactAttributeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8a44546a63583a03bd40b9e86405c3d560b3a94e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464654"
---
# <a name="xactattributeenum"></a>XactAttributeEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica os atributos de transação de um objeto [Connection](connection-object-ado.md).

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
<td><p><strong>adXactAbortRetaining</strong></p></td>
<td><p>262144</p></td>
<td><p>Executa a manutenção de anulações — ou seja, chamar <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> inicia automaticamente uma nova transação. Nem todos os provedores oferecem suporte para isso.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactCommitRetaining</strong></p></td>
<td><p>131072</p></td>
<td><p>Executa a manutenção de confirmações — ou seja, chamar <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> inicia automaticamente uma nova transação. Nem todos os provedores oferecem suporte para isso.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC Equivalente**

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
<td><p>AdoEnums.XactAttribute.ABORTRETAINING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.XactAttribute.COMMITRETAINING</p></td>
</tr>
</tbody>
</table>

