---
title: Instrução ALTER USER ou DATABASE (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f0baf0faab717c35da0313d36e2ec1ac73528255
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879435"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>Instrução ALTER USER ou DATABASE (Microsoft Access SQL)

**Aplica-se a**: Access 2013, o Office 2013

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
<td><p><em>user</em></p></td>
<td><p>O nome de um usuário que será adicionado ao arquivo de informações do grupo de trabalho.</p></td>
</tr>
<tr class="even">
<td><p><em>newpassword</em></p></td>
<td><p>A nova senha que será associada ao nome do <em>usuário</em> ou do <em>banco de dados</em> especificado.</p></td>
</tr>
<tr class="odd">
<td><p><em>oldpassword</em></p></td>
<td><p>A senha existente que será associada ao nome do <em>usuário</em> ou do <em>grupo</em> especificado.</p></td>
</tr>
</tbody>
</table>

