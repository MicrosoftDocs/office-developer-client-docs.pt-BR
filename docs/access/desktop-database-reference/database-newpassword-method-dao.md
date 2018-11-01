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
ms.openlocfilehash: 4b3d4d26a194e2790bf03fcdc5d1911c1e69bbf8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882865"
---
# <a name="databasenewpassword-method-dao"></a>Método Database.NewPassword (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Altera a senha de um banco de dados existente do mecanismo de banco de dados do Microsoft Access (somente espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . NewPassword (***bstrOld***, ***bstrNew***)

*expressão* Uma expressão que retorna um objeto de **banco de dados** .

### <a name="parameters"></a>Parâmetros

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
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>bstrOld</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Cadeia de caracteres</strong></p></td>
<td><p>A configuração atual da propriedade <strong>Password</strong> do objeto <strong>Database</strong>.</p></td>
</tr>
<tr class="even">
<td><p>bstrNew</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Cadeia de caracteres</strong></p></td>
<td><p>A nova configuração da propriedade <strong>Password</strong> do objeto <strong>Database</strong> .</p>

> [!NOTE]
> [!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As senhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

As cadeias de caracteres bstrOld e bstrNew podem ter até 20 caracteres e podem incluir qualquer caractere exceto o caractere ASCII 0 (nulo). Para limpar a senha, use uma cadeia de caracteres de comprimento zero ("") para bstrNew.

Senhas diferenciam maiúsculas de minúsculas.

Se um banco de dados não tiver senha, o mecanismo de banco de dados do Microsoft Access criará uma automaticamente passando uma cadeia de caracteres de comprimento zero ("") para a senha antiga.


> [!IMPORTANT]
> [!IMPORTANTE] Se perder a sua senha, você nunca mais poderá abrir o seu banco de dados.


