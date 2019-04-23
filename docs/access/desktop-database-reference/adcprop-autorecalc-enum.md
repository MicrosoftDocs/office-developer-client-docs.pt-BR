---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e385df5029238106b51aa62949d5e4e94f065657
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280519"
---
# <a name="adcpropautorecalcenum"></a>ADCPROP\_AUTORECALC\_enum

**Aplica-se ao:** Access 2013, Office 2013

Especifica quando o provedor [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) recalcula colunas calculadas e agregadas em um Recordset hierárquico.

Essas constantes são usadas somente com o provedor **MSDataShape** e a propriedade dinâmica "**recálculo automático**" do **Recordset** , que é referenciada no [índice de propriedade dinâmica do ADO](ado-dynamic-property-index.md) e documentada no [serviço de cursor da Microsoft para OLE Banco](microsoft-cursor-service-for-ole-db-ado-service-component.md) [de dados ou documentação do Microsoft Data Shaping Service para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) .

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
<td><p><strong>adRecalcAlways</strong></p></td>
<td><p>1</p></td>
<td><p>Padrão. Recalcula sempre que determinados valores do provedor <strong>MSDataShape</strong>, dos quais as colunas calculadas dependem, são alterados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecalcUpFront</strong></p></td>
<td><p>,0</p></td>
<td><p>Calcula apenas quando cria-se inicialmente o <strong>Recordset</strong> hierárquico.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente do ADO/WFC

Essas constantes não têm ADO/WFC equivalentes.

