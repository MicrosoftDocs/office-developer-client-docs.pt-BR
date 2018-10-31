---
title: REVOGAR instrução (Microsoft Access SQL)
TOCTitle: REVOKE statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4bcdd7aa77823a53ba2a2c0cde4badbac571611a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860543"
---
# <a name="revoke-statement-microsoft-access-sql"></a>REVOGAR instrução (Microsoft Access SQL)

**Aplica-se a**: Access 2013 | Office 2013

Revoga privilégios específicos de um usuário ou grupo existente.

## <a name="syntax"></a>Sintaxe

REVOGAR {*privilégio*\[, *privilégios*,... \]} Diante {tabela *tabela* | OBJETO *objeto*|

*Contêiner*do CONTÊINER} FROM {*authorizationname*\[, *authorizationname*, … \]}

A instrução REVOKE contém estas partes:

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
<td><p><em>privilege</em></p></td>
<td><p>O privilégio ou privilégios a serem revogados. Privilégios são especificados com as seguintes palavras-chave: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA e UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>Nenhum nome de tabela válido.</p></td>
</tr>
<tr class="odd">
<td><p><em>object</em></p></td>
<td><p>Isso pode incluir qualquer objeto não-tabela. Uma consulta armazenada (visualização ou procedimento) é um exemplo.</p></td>
</tr>
<tr class="even">
<td><p><em>container</em></p></td>
<td><p>O nome de um contêiner válido.</p></td>
</tr>
<tr class="odd">
<td><p><em>authorizationname</em></p></td>
<td><p>Um nome de usuário ou grupo.</p></td>
</tr>
</tbody>
</table>

