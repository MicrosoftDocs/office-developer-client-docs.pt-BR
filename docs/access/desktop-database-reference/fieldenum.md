---
title: FieldEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5efcdbd9da4214d7f2b78ffbcfb81fb13265087e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462139"
---
# <a name="fieldenum"></a>FieldEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica os campos especiais mencionados em uma coleção de [Campos](record-object-ado.md) do objeto [Record](fields-collection-ado.md).

**Comentários**

Essas constantes fornecem um "atalho" para acessar os campos especiais associados a um **Record**. Recupere o objeto [Field](field-object-ado.md) da coleção de **Campos** e, em seguida, obtenha seu conteúdo com a propriedade **Value** do objeto [Field](value-property-ado.md).

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
<td><p><strong>adDefaultStream</strong></p></td>
<td><p>-1</p></td>
<td><p>Faz referência ao campo que contém o objeto <a href="stream-object-ado.md">Stream</a> padrão associado a um <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecordURL</strong></p></td>
<td><p>-2</p></td>
<td><p>Faz referência ao campo que contém a sequência de URL absoluto para o <strong>Record</strong> atual.</p></td>
</tr>
</tbody>
</table>

