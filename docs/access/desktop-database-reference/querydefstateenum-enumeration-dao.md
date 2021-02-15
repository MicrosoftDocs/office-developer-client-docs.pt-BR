---
title: Enumeração DeryDefStateEnum (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ca9923b1604b17c1d7f64d2d968378fec4a8c24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303315"
---
# <a name="querydefstateenum-enumeration-dao"></a>Enumeração DeryDefStateEnum (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Usada com a propriedade **Prepare** para especificar o método usado para indicar como uma consulta deve ser preparada.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbQPrepare</p></td>
<td><p>1 </p></td>
<td><p>(Padrão) A instrução é preparada (ou seja, a API de ODBC SQLPrepare é chamada).</p></td>
</tr>
<tr class="even">
<td><p>dbQUnprepare</p></td>
<td><p>2 </p></td>
<td><p>A instrução não é preparada (ou seja, a API de ODBC SQLExecDirect é chamada).</p></td>
</tr>
</tbody>
</table>

