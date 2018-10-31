---
title: RuleEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: RuleEnum
ms:assetid: 5b59f202-315b-09b7-8505-9ac08ceccb3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249317(v=office.15)
ms:contentKeyID: 48545071
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c7c930ddd550d7c919b033e098bc95fa03806bbc
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863539"
---
# <a name="ruleenum"></a>RuleEnum

**Aplica-se a**: Access 2013 | Office 2013

Especifica a regra a ser seguida quando uma [Chave](key-object-adox.md) é excluída.

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
<td><p><strong>adRICascade</strong></p></td>
<td><p>1</p></td>
<td><p>Alterações em cascata.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRINone</strong></p></td>
<td><p>0</p></td>
<td><p>Padrão. Nenhuma ação é executada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRISetDefault</strong></p></td>
<td><p>3</p></td>
<td><p>A chave estrangeira é definida como o padrão.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRISetNull</strong></p></td>
<td><p>2</p></td>
<td><p>O valor da chave estrangeira é definido como nulo.</p></td>
</tr>
</tbody>
</table>

