---
title: Instrução DROP USER ou GROUP (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5cf75de06c13e2452e5f33b8355b7fb480d8a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462482"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>Instrução DROP USER ou GROUP (Microsoft Access SQL)


**Aplica-se a**: Access 2013 | Office 2013

Exclui um ou mais *usuários* ou *grupos* ou remove um ou mais *usuários* existentes de um *grupo* existente.

## <a name="syntax"></a>Sintaxe

Excluir um ou mais *usuários* ou remover um ou mais *usuários* de um *grupo*:

DROP USER *usuário*\[, *usuário*,... \] \[De *grupo*\]

Excluir um ou mais *grupos*:

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
<td><p><em>group</em></p></td>
<td><p>O nome de um grupo a ser removido do arquivo de informações do grupo de trabalho.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Se a palavra-chave FROM for utilizada na instrução DROP USER, cada um dos *usuários* listados na instrução será removido do *grupo* especificado, seguinte à palavra-chave FROM. Entretanto, os próprios *usuários* não serão excluídos.

A instrução DROP GROUP excluirá o(s) *grupo*(s) especificado(s). Os *usuários* que são membros do(s) *grupo*(s) não serão afetados, mas eles não serão mais membros do(s) *grupo*(s) excluídos.

