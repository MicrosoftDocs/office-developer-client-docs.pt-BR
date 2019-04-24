---
title: Enumeração de UpdateTypeEnum (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d1e4ecbc216ab4a00dabd85f623bc134772dfd4c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306185"
---
# <a name="updatetypeenum-enumeration-dao"></a>Enumeração de UpdateTypeEnum (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Usada com o método **Update** para especificar quais atualizações devem ser gravadas no disco.

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
<td><p>dbUpdateBatch</p></td>
<td><p>quatro</p></td>
<td><p>Todas as atualizações pendentes do cache de atualização são gravadas no disco.</p></td>
</tr>
<tr class="even">
<td><p>dbUpdateCurrentRecord</p></td>
<td><p>duas</p></td>
<td><p>Somente as alterações pendentes do registro atual são gravadas no disco.</p></td>
</tr>
<tr class="odd">
<td><p>dbUpdateRegular</p></td>
<td><p>1</p></td>
<td><p>(Padrão) As alterações pendentes não são armazenadas em cache e são gravadas no disco imediatamente.</p></td>
</tr>
</tbody>
</table>

