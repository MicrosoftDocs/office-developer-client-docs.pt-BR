---
title: Enumeração RecordStatusEnum (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c2d96c359a913660c146f4850a1846554e3b6856
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875116"
---
# <a name="recordstatusenum-enumeration-dao"></a>Enumeração RecordStatusEnum (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Usada com a propriedade **RecordStatus** para indicar o status de atualização do registro atual, se ele fizer parte de uma atualização em lotes.

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
<td><p>dbRecordDBDeleted</p></td>
<td><p>4</p></td>
<td><p>O registro foi excluído localmente e no banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>dbRecordDeleted</p></td>
<td><p>3</p></td>
<td><p>O registro foi excluído, mas ainda não foi excluído do banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>dbRecordModified</p></td>
<td><p>1</p></td>
<td><p>O registro foi modificado e não foi atualizado no banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>dbRecordNew</p></td>
<td><p>2</p></td>
<td><p>O registro foi inserido com o método <strong>AddNew</strong>, mas ainda não foi inserido no banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>dbRecordUnmodified</p></td>
<td><p>0</p></td>
<td><p>(Padrão) O registro não foi modificado ou foi atualizado com êxito.</p></td>
</tr>
</tbody>
</table>

