---
title: Instrução CREATE USER ou GROUP (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b294af16498778eae94b38a7a31b93fd029585e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295377"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>Instrução CREATE USER ou GROUP (Microsoft Access SQL)

**Aplica-se ao:** Access 2013, Office 2013

Cria um ou mais usuários ou grupos novos.

## <a name="syntax"></a>Sintaxe

### <a name="create-a-user"></a>Criar um usuário

Create User *User* *password PID* \[, *User* *password PID*,...\]

### <a name="create-a-group"></a>Criar um grupo

Criar *grupo* de grupo *pid*\[, *pid*de *grupo* ,...\]

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
<td><p><em>usuário</em></p></td>
<td><p>O nome de um usuário a ser adicionado ao arquivo de informações do grupo de trabalho.</p></td>
</tr>
<tr class="even">
<td><p><em>grupo</em></p></td>
<td><p>O nome de um grupo a ser adicionado ao arquivo de informações do grupo de trabalho.</p></td>
</tr>
<tr class="odd">
<td><p><em>la</em></p></td>
<td><p>A senha a ser associada ao nome de <em>usuário</em> especificado.</p></td>
</tr>
<tr class="even">
<td><p><em>atos</em></p></td>
<td><p>A identificação pessoal.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Um *usuário* e um *grupo* não podem ter o mesmo nome.

Uma *senha* é exigida para cada *usuário* ou *grupo* que é criado.

