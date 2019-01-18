---
title: InheritTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba1a78e49d44bce0c489e4f5259ec9699543e231
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706804"
---
# <a name="inherittypeenum"></a>InheritTypeEnum

**Aplica-se a**: Access 2013, o Office 2013

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
<td><p>3</p></td>
<td><p>Os objetos e os outros contêineres existentes no objeto principal herdam a entrada.</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritContainers</strong></p></td>
<td><p>2</p></td>
<td><p>Outros contêineres existentes no objeto principal herdam a entrada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adInheritNone</strong></p></td>
<td><p>0</p></td>
<td><p>Padrão. Nada é herdado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritNoPropagate</strong></p></td>
<td><p>4</p></td>
<td><p>Os sinalizadores <strong>adInheritObjects</strong> e <strong>adInheritContainers</strong> não são propagados para uma entrada herdada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adInheritObjects</strong></p></td>
<td><p>1</p></td>
<td><p>Os objetos não contêiner existentes no contêiner herdam as permissões.</p></td>
</tr>
</tbody>
</table>

