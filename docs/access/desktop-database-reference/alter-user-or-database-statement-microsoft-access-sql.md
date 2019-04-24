---
title: Instrução ALTER USER ou DATABASE (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297176"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>Instrução ALTER USER ou DATABASE (Microsoft Access SQL)

**Aplica-se ao:** Access 2013, Office 2013

Altera a senha de um usuário existente ou de um banco de dados.

## <a name="syntax"></a>Sintaxe

ALTER DATABASE PASSWORD *novasenha senhaantiga*

ALTER USER *usuário* PASSWORD *novasenha senhaantiga*

A instrução ALTER USER ou DATABASE possui as seguintes partes:

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
<td><p>O nome de um usuário que será adicionado ao arquivo de informações do grupo de trabalho.</p></td>
</tr>
<tr class="even">
<td><p><em>newPassword</em></p></td>
<td><p>A nova senha que será associada ao nome do <em>usuário</em> ou do <em>banco de dados</em> especificado.</p></td>
</tr>
<tr class="odd">
<td><p><em>SenhaAntiga</em></p></td>
<td><p>A senha existente que será associada ao nome do <em>usuário</em> ou do <em>grupo</em> especificado.</p></td>
</tr>
</tbody>
</table>

