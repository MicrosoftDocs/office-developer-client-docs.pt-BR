---
title: Bloco de dados CriarRegistro
TOCTitle: CreateRecord data block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63e189143e77f9fcc42fa8d48c3ebfb2feda6633
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719808"
---
# <a name="createrecord-data-block"></a>Bloco de dados CriarRegistro


**Aplica-se a**: Access 2013, o Office 2013

Você pode usar o bloco de dados **CriarRegistro** para criar um novo registro na tabela especificada.

> [!NOTE]
> [!OBSERVAçãO] O bloco de dados **CriarRegistro** está disponível somente em Macros de Dados.

## <a name="setting"></a>Configuração

O bloco de dados **ExcluirRegistro** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Obrigatório</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Criar Registro em</strong></p></td>
<td><p>Sim</p></td>
<td><p>O nome da tabela onde o novo registro será criado.</p></td>
</tr>
<tr class="even">
<td><p><strong>Alias</strong></p></td>
<td><p>Não</p></td>
<td><p>Uma cadeia de caracteres que identifica o registro. Você pode usar o alias do registro para identificá-lo</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O registro criado por **CriarRegistro** se torna automaticamente o registro atual.

Após a instrução **CriarRegistro** , você pode inserir um bloco de comandos que executará antes o novo registro é submetido. As ações a seguir estão disponíveis em bloco de dados **CriarRegistro**.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="cancelrecordchange-macro-action.md">Ação da macro CancelarAlteraçãodeRegistro</a></p></td>
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
<td><p><a href="setfield-macro-action.md">Ação da macro DefinirCampo</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">Ação da macro DefinirVarLocal</a></p></td>
</tr>
</tbody>
</table>


Depois que a ação **CriarRegistro** criar um registro, use a ação **DefinirCampo** para especificar o valor de um campo no novo registro.

Você pode usar uma instrução **Se...Então...Senão** para executar operações com base em uma condição.

Para cancelar a criação de um registro, use a ação **CancelarAlteraçãodeRegistro**. Dessa forma, as alterações não são atribuídas e o bloco de dados **CriarRegistro** é encerrado.

Quando o novo registro for atribuído, você poderá usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o registro. Por exemplo, use a sintaxe a seguir para se referir ao campo AssignedTo do registro mais recentemente criado.

`[LastCreateRecordIdentity].[AssignedTo]`

O bloco de dados **CriarRegistro** somente pode ser usado nos eventos de macro de dados **[Após Inserir](after-insert-macro-event.md)**, **[Após Atualizar](after-update-macro-event.md)** e **[Após Atualizar](after-update-macro-event.md)**.

