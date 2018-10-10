---
title: Instrução GRANT (Microsoft Access SQL)
TOCTitle: GRANT Statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d4fffc9ac40586be899de0dd4054ba39dd3a6489
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461985"
---
# <a name="grant-statement-microsoft-access-sql"></a>Instrução GRANT (Microsoft Access SQL)


**Aplica-se a**: Access 2013 | Office 2013

Concede privilégios específicos a um usuário ou grupo existente.

## <a name="syntax"></a>Sintaxe

GRANT {*privilégio*\[, *privilégios*,... \]} Diante {tabela *tabela* | OBJETO *objeto*|

CONTAINER *contêiner* } TO {*authorizationname*\[, *authorizationname*, … \]}

A instrução GRANT tem estas partes:

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
<td><p>O privilégio ou privilégios a serem concedidos. Privilégios são especificados com as seguintes palavras-chave: selecionar, excluir, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA e UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>tablename</em></p></td>
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

