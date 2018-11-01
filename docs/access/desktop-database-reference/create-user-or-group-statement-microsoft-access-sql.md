---
title: Instrução CREATE USER ou GROUP (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: cd33755800d0ed820a9690a6910f3edf064c3c82
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872190"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>Instrução CREATE USER ou GROUP (Microsoft Access SQL)

**Aplica-se a**: Access 2013, o Office 2013

Cria um ou mais usuários ou grupos novos.

## <a name="syntax"></a>Sintaxe

**Criar um usuário**:

CREATE USER *usuário* *senha pid* \[, *usuário* *senha pid*,...\]

**Criar um grupo**:

Criar grupo *grupo* *pid*\[, *grupo* *pid*, …\]

A instrução CREATE USER ou GROUP tem estas partes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>user</em></p></td>
<td><p>O nome de um usuário que será adicionado ao arquivo de informações do grupo de trabalho.</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>O nome de um grupo a ser adicionado ao arquivo de informações do grupo de trabalho.</p></td>
</tr>
<tr class="odd">
<td><p><em>password</em></p></td>
<td><p>A senha a ser associada ao nome de <em>usuário</em> especificado.</p></td>
</tr>
<tr class="even">
<td><p><em>pid</em></p></td>
<td><p>A identificação pessoal.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Um *usuário* e um *grupo* não podem ter o mesmo nome.

Uma *senha* é necessária para cada *usuário* ou *grupo* que é criado.

