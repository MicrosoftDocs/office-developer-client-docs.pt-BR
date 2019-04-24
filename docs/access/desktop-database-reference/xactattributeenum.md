---
title: XactAttributeEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e79a6143c65637660b2d59b7c7efb6a21e8935bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302566"
---
# <a name="xactattributeenum"></a>XactAttributeEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica os atributos de transação de um objeto [Connection](connection-object-ado.md).

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
<td><p><strong>adXactAbortRetaining</strong></p></td>
<td><p>262144</p></td>
<td><p>Realiza anulações de retenção; ou seja, chamar <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> iniciará automaticamente uma nova transação. Nem todos os provedores oferecem suporte para isso.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactCommitRetaining</strong></p></td>
<td><p>131072</p></td>
<td><p>Realiza confirmações de retenção; ou seja, a chamada do <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> iniciará automaticamente uma nova transação. Nem todos os provedores oferecem suporte para isso.</p></td>
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
<td><p>AdoEnums. XactAttribute. ABORTRETAINING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. XactAttribute. COMMITRETAINING</p></td>
</tr>
</tbody>
</table>

