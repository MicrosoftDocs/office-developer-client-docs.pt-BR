---
title: Bloco de dados EditarRegistro
TOCTitle: EditRecord Data Block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 07763e32e0f8687816dc39298f91733ca814d275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461997"
---
# <a name="editrecord-data-block"></a>Bloco de dados EditarRegistro

**Aplica-se a**: Access 2013 | Office 2013

Você pode usar o bloco de dados **EditarRegistro** para alterar os valores contidos em um registro existente.

> [!NOTE]
> [!OBSERVAçãO] O bloco de dados **EditarRegistro** está disponível somente em Macros de Dados.


## <a name="setting"></a>Configuração

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
<td><p><a href="cancelrecordchange-macro-action.md">Ação de macro CancelRecordChange</a></p></td>
</tr>
<tr class="even">
<td><p><a href="comment-macro-statement.md">Instrução de macro de comentário</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="group-macro-statement.md">Instrução de macro de grupo</a></p></td>
</tr>
<tr class="even">
<td><p><a href="if-then-else-macro-block.md">Se... Então... Instrução de Macro Else</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">Ação de macro SetField</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">Ação de macro SetLocalVar</a></p></td>
</tr>
</tbody>
</table>

Use a ação **DefinirCampo** para especificar os novos valores de um campo no registro editado.

Você pode usar uma instrução **Se...Então...Senão** para executar operações com base em uma condição.

Para cancelar a edição de um registro, use a ação **CancelarAlteraçãodeRegistro**. Dessa forma, as alterações não são atribuídas e o bloco de dados **EditarRegistro** é encerrado.

Você pode usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o último registro criado em um bloco de dados **CriarRegistro**. Por exemplo, use a sintaxe a seguir para se referir ao campo AssignedTo do registro mais recentemente criado:

`[LastCreateRecordIdentity].[AssignedTo]`

O bloco de dados CriarRegistro somente pode ser usado nos eventos de macro de dados **[Após Inserir](after-insert-macro-event.md)**, **[Após Atualizar](after-update-macro-event.md)** e **[Após Atualizar](after-update-macro-event.md)**.

