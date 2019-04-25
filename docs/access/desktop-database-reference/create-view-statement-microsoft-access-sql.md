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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295363"
---
# <a name="create-view-statement-microsoft-access-sql"></a>Instrução CREATE VIEW (Microsoft Access SQL)

**Aplica-se ao**: Access 2013, Office 2013

Cria uma nova exibição.

> [!NOTE]
> O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de CREATE VIEW ou de qualquer uma das instruções DDL com bancos de dados de mecanismos de banco de dados que não são do Microsoft Access.

## <a name="syntax"></a>Sintaxe

CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*

A instrução CREATE VIEW tem as seguintes partes:

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
<td><p><em>view</em></p></td>
<td><p>O nome do modo de exibição a ser criado.</p></td>
</tr>
<tr class="even">
<td><p><em>campo1</em>, <em>campo2</em></p></td>
<td><p>O nome do campo ou campos para os campos correspondentes especificados no <em>selectstatement</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>selectstatement</em></p></td>
<td><p>Uma instrução SQL SELECT. Para obter mais informações, confira <a href="select-statement-microsoft-access-sql.md">Instrução SELECT</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A instrução SELECT que define a exibição não pode ser uma instrução [SELECT INTO](select-into-statement-microsoft-access-sql.md).

A declaração SELECT que define o modo de exibição não pode conter parâmetros.

O nome da exibição não pode ser igual ao nome de uma tabela existente.

Se a consulta definida pela instrução SELECT for atualizável, a exibição também será atualizável. Caso contrário, o modo de exibição será somente leitura.

Se os dois campos na consulta definidos pela instrução SELECT tiverem o mesmo nome, a definição do modo de exibição deverá incluir uma lista de campos especificando nomes exclusivos para cada um dos campos na consulta.

