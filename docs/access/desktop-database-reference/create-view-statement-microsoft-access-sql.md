---
title: Instrução CREATE VIEW (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 73fac5ff9dd1f5cf277b8cb241044af23609b764
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706622"
---
# <a name="create-view-statement-microsoft-access-sql"></a>Instrução CREATE VIEW (Microsoft Access SQL)

**Aplica-se a**: Access 2013, o Office 2013

Cria uma nova exibição.

> [!NOTE]
> [!OBSERVAçãO] O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de CREATE VIEW nem de nenhuma instrução DDL, com os bancos de dados cujos mecanismos sejam diferentes do Microsoft Access.

## <a name="syntax"></a>Sintaxe

*Modo de exibição* de CREATE VIEW \[(*field1*\[, *field2*\[,... \] \])\] Como *selectstatement*

A instrução CREATE VIEW contém estas partes:

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
<td><p><em>view</em></p></td>
<td><p>O nome da exibição a ser criada.</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>O nome do(s) campo(s) para a correspondência de campos especificada em <em>selectstatement</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>selectstatement</em></p></td>
<td><p>Uma instrução SQL SELECT. Para obter mais informações, consulte a <a href="select-statement-microsoft-access-sql.md">instrução SELECT</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A instrução SELECT que define a exibição não pode ser uma instrução [SELECT INTO](select-into-statement-microsoft-access-sql.md).

A instrução SELECT que define a exibição não pode conter nenhum parâmetro.

O nome do modo de exibição não pode ser igual ao nome de uma tabela existente.

Se a consulta definida pela instrução SELECT for atualizável, a exibição também é atualizável. Caso contrário, a exibição será somente leitura.

Se dois campos na consulta definida pela instrução SELECT tiverem o mesmo nome, a definição de exibição deverá incluir uma lista de campos que especifique nomes exclusivos para cada um dos campos na consulta.

