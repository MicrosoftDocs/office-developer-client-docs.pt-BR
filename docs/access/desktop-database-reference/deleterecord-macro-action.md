---
title: Ação da macro ExcluirRegistro
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8fb20068052972696b09ea0d2165b344e97ea922
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725949"
---
# <a name="deleterecord-macro-action"></a>Ação da macro ExcluirRegistro

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

