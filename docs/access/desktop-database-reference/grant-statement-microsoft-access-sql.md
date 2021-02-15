---
title: Instrução GRANT (Microsoft Access SQL)
TOCTitle: GRANT statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4357099f8bcb9b2308b5cda3543949765b8c3420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292129"
---
# <a name="grant-statement-microsoft-access-sql"></a>Instrução GRANT (Microsoft Access SQL)

**Aplica-se ao:** Access 2013, Office 2013

Concede privilégios específicos a um usuário ou grupo existente.

## <a name="syntax"></a>Sintaxe

GRANT {*privilege* \[ , *privilege*, ... \] } Tabela *ON{|* Objeto *OBJECT*|

CONTÊINER *container* } TO {*authorizationname* \[ , *authorizationname*, ... \] }

A instrução GRANT tem estas partes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Sair</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>privilege</em></p></td>
<td><p>O privilégio ou os privilégios a serem concedidos. Os privilégios são especificados usando-se as seguintes palavras-chave: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA e UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>tablename</em></p></td>
<td><p>Nenhum nome de tabela válido.</p></td>
</tr>
<tr class="odd">
<td><p><em>objeto</em></p></td>
<td><p>Isso pode incluir qualquer objeto não-tabela. Uma consulta armazenada (visualização ou procedimento) é um exemplo.</p></td>
</tr>
<tr class="even">
<td><p><em>contêiner</em></p></td>
<td><p>O nome de um contêiner válido.</p></td>
</tr>
<tr class="odd">
<td><p><em>authorizationname</em></p></td>
<td><p>Um nome de usuário ou grupo.</p></td>
</tr>
</tbody>
</table>

