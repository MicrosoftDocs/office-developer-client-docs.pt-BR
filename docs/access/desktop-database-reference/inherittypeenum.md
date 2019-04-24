---
title: InheritTypeEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba1a78e49d44bce0c489e4f5259ec9699543e231
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291411"
---
# <a name="inherittypeenum"></a>InheritTypeEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica como os objetos herdarão permissões definidas com [SetPermissions](setpermissions-method-adox.md).

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
<td><p><strong>adInheritBoth</strong></p></td>
<td><p>3D</p></td>
<td><p>Os objetos e os outros contêineres existentes no objeto principal herdam a entrada.</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritContainers</strong></p></td>
<td><p>duas</p></td>
<td><p>Outros contêineres existentes no objeto principal herdam a entrada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adInheritNone</strong></p></td>
<td><p>,0</p></td>
<td><p>Padrão. Nada é herdado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritNoPropagate</strong></p></td>
<td><p>quatro</p></td>
<td><p>Os sinalizadores <strong>adInheritObjects</strong> e <strong>adInheritContainers</strong> não são propagados para uma entrada herdada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adInheritObjects</strong></p></td>
<td><p>1</p></td>
<td><p>Os objetos não contêiner existentes no contêiner herdam as permissões.</p></td>
</tr>
</tbody>
</table>

