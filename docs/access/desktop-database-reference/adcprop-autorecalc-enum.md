---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc02e8cde556a70ca6b2c72f056d218904c31ec2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465003"
---
# <a name="adcpropautorecalcenum"></a>ADCPROP\_AUTORECALC\_ENUM

**Aplica-se a**: Access 2013 | Office 2013

Especifica quando o provedor [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) recalcula colunas calculadas e agregadas em um Recordset hierárquico.

Essas constantes são usadas somente com o provedor **MSDataShape** e a **Recordset** "**Auto Recalc**" propriedade dinâmica, que é referenciada no [Índice de propriedades dinâmicas ADO](ado-dynamic-property-index.md) e documentada no [Microsoft Cursor Service para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) ou a documentação do [Microsoft Data Shaping Service para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) .

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
<td><p><strong>adRecalcAlways</strong></p></td>
<td><p>1</p></td>
<td><p>Padrão. Recalcula sempre que determinados valores do provedor <strong>MSDataShape</strong>, dos quais as colunas calculadas dependem, são alterados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecalcUpFront</strong></p></td>
<td><p>0</p></td>
<td><p>Calcula apenas quando cria-se inicialmente o <strong>Recordset</strong> hierárquico.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC Equivalente**

Essas constantes não têm ADO/WFC equivalentes.

