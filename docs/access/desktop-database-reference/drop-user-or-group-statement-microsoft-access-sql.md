---
title: Instrução DROP USER ou GROUP (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 995f935ceea5af3b740215c5a4137e02e7ebb1b2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700833"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>Instrução DROP USER ou GROUP (Microsoft Access SQL)

**Aplica-se a**: Access 2013, o Office 2013

Exclui um ou mais existentes *usuários* ou *grupos*ou remove um ou mais *usuários* existentes de um *grupo*de existente.

## <a name="syntax"></a>Sintaxe

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a>Excluir um ou mais usuários ou remover um ou mais usuários de um grupo

DROP USER *usuário*\[, *usuário*,... \] \[De *grupo*\]

### <a name="delete-one-or-more-groups"></a>Excluir um ou mais grupos

DROP GROUP *grupo*\[, *grupo*,...\]

A instrução DROP USER ou GROUP tem estas partes:

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
<td><p>O nome de um usuário a ser removido do arquivo de informações do grupo de trabalho.</p></td>
</tr>
<tr class="even">
<td><p><em>grupo</em></p></td>
<td><p>O nome de um grupo a ser removido do arquivo de informações do grupo de trabalho.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Se a palavra-chave FROM for usada na instrução DROP USER, cada um dos *usuários* listados na instrução será removido do *grupo* especificado após a palavra-chave FROM. No entanto, os *usuários* sozinhos não serão excluídos.

A instrução DROP GROUP excluirá o *grupo*especificado (s). Os *usuários* que são membros do *grupo*(s) não serão afetados, mas eles deixará de ser membros do *grupo*excluído (s).

