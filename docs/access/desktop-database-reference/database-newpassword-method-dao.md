---
title: Método Database.NewPassword (DAO)
TOCTitle: NewPassword Method
ms:assetid: 01c1c454-d651-222c-225a-2b02734a1b7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844754(v=office.15)
ms:contentKeyID: 48542941
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052943
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20f09dbfba50526409472f7eb804ba2c47e4d1d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294852"
---
# <a name="databasenewpassword-method-dao"></a>Método Database.NewPassword (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Altera a senha de um banco de dados existente do mecanismo de banco de dados do Microsoft Access (somente espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . NewPassword(***bstrOld***, ***bstrNew***)

*expressão* Uma expressão que retorna um **objeto Database** .

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Necessária/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>bstrOld</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>A configuração atual da propriedade <strong>Password</strong> do objeto <strong>Database</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>bstrNew</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>A nova configuração da <strong>propriedade Password</strong> do objeto <strong>Database</strong> .</p>
<p><strong>OBSERVAÇÃO:</strong>use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As enhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: Casa27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

As cadeias de caracteres bstrOld e bstrNew podem ter até 20 caracteres e podem incluir qualquer caractere, exceto o caractere ASCII 0 (nulo). Para limpar a senha, use uma cadeia de caracteres de comprimento zero ("") para bstrNew.

Senhas diferenciam maiúsculas de minúsculas.

Se um banco de dados não tiver senha, o mecanismo de banco de dados do Microsoft Access criará uma automaticamente passando uma cadeia de caracteres de comprimento zero ("") para a senha antiga.


> [!IMPORTANT]
> [!IMPORTANTE] Se perder a sua senha, você nunca mais poderá abrir o seu banco de dados.


