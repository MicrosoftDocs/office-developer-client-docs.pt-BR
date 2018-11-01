---
title: Instrução ADD USER (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7a27874a7264258fee51f90fabaeecd180d7aeae
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868606"
---
# <a name="add-user-statement-microsoft-access-sql"></a>Instrução ADD USER (Microsoft Access SQL)

**Aplica-se a**: Access 2013, o Office 2013

Adiciona um ou vários *usuários* existentes em um *grupo* existente.

## <a name="syntax"></a>Sintaxe

Adicionar usuário *usuário*\[, *usuário*,... \] Ao *grupo*

A instrução ADD USER possui as seguintes partes:

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
</tbody>
</table>


## <a name="remarks"></a>Comentários

Depois que um *usuário* tiver sido adicionado a um *grupo*, o *usuário* tem todas as permissões que tiverem sido concedidas ao *grupo*.

