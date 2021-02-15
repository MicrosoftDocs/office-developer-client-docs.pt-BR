---
title: Bloco de dados EditarRegiscord
TOCTitle: EditRecord data block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 32ddfbbf21e62d5967fa1f2f31bab0222664eb39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293592"
---
# <a name="editrecord-data-block"></a>Bloco de dados EditarRegiscord

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar o bloco de dados **EditarRegistro** para alterar os valores contidos em um registro existente.

> [!NOTE]
> O bloco de dados **EditarRegistro** está disponível somente em Macros de Dados.


## <a name="setting"></a>Setting

O bloco de dados **EditarRegistro** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Uma cadeia de caracteres que identifica o registro a ser editado. Se o argumento <em>Alias</em> não for especificado, o registro atual será editado.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentários

Após a instrução **EditarRegistro**, você pode inserir um bloco de comandos que será executado antes da atribuição das alterações do registro. As ações a seguir estão disponíveis em bloco de dados **EditarRegistro**.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="cancelrecordchange-macro-action.md">Ação de macro CancelarAlteraçãodeRegistro</a></p></td>
</tr>
<tr class="even">
<td><p><a href="comment-macro-statement.md">Instrução de macro Comentário</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="group-macro-statement.md">Instrução de macro Grupo</a></p></td>
</tr>
<tr class="even">
<td><p><a href="if-then-else-macro-block.md">Se... Então... Instrução de macro Else</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">Ação de macro DefinirCampo</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">Ação de macro DefinirVarLocal</a></p></td>
</tr>
</tbody>
</table>

Use a ação **DefinirCampo** para especificar os novos valores de um campo no registro editado.

Você pode usar uma instrução **Se...Então...Senão** para executar operações com base em uma condição.

Para cancelar a edição de um registro, use a ação **CancelarAlteraçãodeRegistro**. Dessa forma, as alterações não são atribuídas e o bloco de dados **EditarRegistro** é encerrado.

Você pode usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o último registro criado em um bloco de dados **CriarRegistro**. Por exemplo, use a sintaxe a seguir para se referir ao campo AtribuídoA do registro criado mais recentemente:

`[LastCreateRecordIdentity].[AssignedTo]`

O bloco de dados CriarRegistro somente pode ser usado nos eventos de macro de dados **[Após Inserir](after-insert-macro-event.md)**, **[Após Atualizar](after-update-macro-event.md)** e **[Após Atualizar](after-update-macro-event.md)**.

