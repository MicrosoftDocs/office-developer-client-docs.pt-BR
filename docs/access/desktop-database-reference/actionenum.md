---
title: ActionEnum (referência do banco de dados da área de trabalho do Access)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f098adb42df39d1509a6d22decd8d2cead684f11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280653"
---
# <a name="actionenum"></a>ActionEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica o tipo de ação a ser executada quando [SetPermissions](setpermissions-method-adox.md) é chamado.

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
<td><p><strong>adAccessDeny</strong></p></td>
<td><p>3 </p></td>
<td><p>As permissões especificadas serão negadas ao grupo ou usuário.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAccessGrant</strong></p></td>
<td><p>1 </p></td>
<td><p>O grupo ou usuário terá, pelo menos, as permissões solicitadas.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAccessRevoke</strong></p></td>
<td><p>4 </p></td>
<td><p>Serão revogados todos os direitos de acesso explícitos do grupo ou do usuário.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAccessSet</strong></p></td>
<td><p>2 </p></td>
<td><p>O grupo ou usuário terá exatamente as permissões solicitadas.</p></td>
</tr>
</tbody>
</table>

