---
title: RecordTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: RecordTypeEnum
ms:assetid: 7edd6508-1507-4649-f1aa-03f1873ef09c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249534(v=office.15)
ms:contentKeyID: 48545890
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4eedd04b630e0cc1cf855eefe09bd071dfbbbb50
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464571"
---
# <a name="recordtypeenum"></a>RecordTypeEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica o tipo de objeto [Record](record-object-ado.md).

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
<td><p><strong>adSimpleRecord</strong></p></td>
<td><p>0</p></td>
<td><p>Indica um registro <em>simples</em> (não contém nós filho).</p></td>
</tr>
<tr class="even">
<td><p><strong>adCollectionRecord</strong></p></td>
<td><p>1</p></td>
<td><p>Indica um registro de <em>coleção</em> (contém nós filho).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecordUnknown</strong></p></td>
<td><p>-1</p></td>
<td><p>Indica que o tipo deste <strong>Record</strong> é desconhecido.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStructDoc</strong></p></td>
<td><p>2</p></td>
<td><p>Indica um tipo especial de registro de <em>coleção</em> que representa documentos COM estruturados.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC Equivalente**

Essas constantes não têm ADO/WFC equivalentes.

