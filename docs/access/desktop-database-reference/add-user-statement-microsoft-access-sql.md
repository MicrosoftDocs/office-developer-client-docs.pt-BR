---
title: Instrução ADD USER (Microsoft Access SQL)
TOCTitle: ADD USER Statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba08ab3104fa08780e8affa310b52a65f67d8831
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463761"
---
# <a name="add-user-statement-microsoft-access-sql"></a>Instrução ADD USER (Microsoft Access SQL)

**Aplica-se a**: Access 2013 | Office 2013

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

Assim que um *usuário* tiver sido adicionado a um *grupo*, o *usuário* terá todas as permissões concedidas ao *grupo*.

