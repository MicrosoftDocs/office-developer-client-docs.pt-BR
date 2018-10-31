---
title: SaveOptionsEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: ffd37090b264e434b5fd3750f474122f8da4bfbb
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861901"
---
# <a name="saveoptionsenum"></a>SaveOptionsEnum

**Aplica-se a**: Access 2013 | Office 2013

Especifica se um arquivo deveria ser criado ou sobregravado ao salvar a partir de um objeto [Stream](stream-object-ado.md). Os valores podem ser combinados com um operador AND.

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


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Essas constantes não têm ADO/WFC equivalentes.

