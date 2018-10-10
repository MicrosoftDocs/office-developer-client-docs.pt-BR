---
title: SaveOptionsEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68526eca205fb41dd2789ec187514d0f9b11e35f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462876"
---
# <a name="saveoptionsenum"></a>SaveOptionsEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica se um arquivo deveria ser criado ou sobregravado ao salvar a partir de um objeto [Stream](stream-object-ado.md). Os valores podem ser combinados com um operador AND.

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
<td><p><strong>adSaveCreateNotExist</strong></p></td>
<td><p>1</p></td>
<td><p>Padrão. Crie um novo arquivo se o arquivo especificado pelo parâmetro <em>FileName</em> ainda não existir.</p></td>
</tr>
<tr class="even">
<td><p><strong>adSaveCreateOverWrite</strong></p></td>
<td><p>2</p></td>
<td><p>Sobregrava o arquivo com os dados a partir do objeto <strong>Stream</strong> aberto no momento se o arquivo especificado pelo parâmetro <em>Filename</em> já existir.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC Equivalente**

Essas constantes não têm ADO/WFC equivalentes.
