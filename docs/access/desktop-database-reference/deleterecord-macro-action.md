---
title: Ação de macro ExcluirRegistro
TOCTitle: DeleteRecord Macro Action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 17cc677ed5762c6274db80105cdf8e899565ecb9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880877"
---
# <a name="deleterecord-macro-action"></a>Ação de macro ExcluirRegistro

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **ExcluirRegistro** para excluir um registro.

## <a name="setting"></a>Configuração

O bloco de dados **ExcluirRegistro** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Alias de Registro</strong></p></td>
<td><p>Uma cadeia de caracteres que identifica o registro a ser excluído. Se o argumento <em>Alias</em> não for especificado, o registro atual será excluído.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentários

Você pode usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o último registro criado em um bloco de dados **CriarRegistro**. Por exemplo, use a seguinte sintaxe para referir-se o registro mais recentemente criado:

`[LastCreateRecordIdentity]`

