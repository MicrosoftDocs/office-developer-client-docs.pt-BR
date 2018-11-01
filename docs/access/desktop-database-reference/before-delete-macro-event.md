---
title: Evento de macro Antes de Excluir
TOCTitle: Before Delete Macro Event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0ee4878a742454eb1b02f4b9a45c14ad79097c46
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876257"
---
# <a name="before-delete-macro-event"></a>Evento de macro Antes de Excluir

**Aplica-se a**: Access 2013, o Office 2013

O evento **Antes de Excluir** ocorre quando um registro é excluído, mas antes da alteração ser submetida.

> [!NOTE]
> [!OBSERVAçãO] O evento **Antes de Excluir** está disponível somente em Macros de Dados.

## <a name="remarks"></a>Comentários

Use o evento **Antes de Excluir** para executar qualquer ação que você deseja que ocorra antes da exclusão de um registro. O **Antes de Alterar** é comumente usado para executar validação e criar mensagens de erro personalizadas.

Você pode acessar um valor no registro a ser excluído utilizando a seguinte sintaxe:

`[Old].[Field Name]`

Por exemplo, para acessar o valor do campo Quantidadeemestoque no registro a ser excluído, use a seguinte sintaxe:

`[Old].[QuantityInStock]`

Os valores contidos no registro a ser excluído são excluídos permanentemente após a conclusão do evento **Antes de Excluir**.

Você pode cancelar o evento **Antes de Excluir** utilizando a ação **GerarErro**. Quando um erro é gerado, as alterações contidas no evento **Antes de excluir** são descartadas.

A tabela a seguir lista comandos de macro que podem ser usadas no evento **Antes de Excluir**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de comando</p></th>
<th><p>Comando</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Fluxo do programa</p></td>
<td><p><a href="comment-macro-statement.md">Instrução de macro de comentário</a></p></td>
</tr>
<tr class="even">
<td><p>Fluxo do programa</p></td>
<td><p><a href="group-macro-statement.md">Instrução de macro de grupo</a></p></td>
</tr>
<tr class="odd">
<td><p>Fluxo do programa</p></td>
<td><p><a href="if-then-else-macro-block.md">Bloco de macro If...Then...Else</a></p></td>
</tr>
<tr class="even">
<td><p>Bloco de dados</p></td>
<td><p><a href="lookuprecord-data-block.md">Ação de Macro Pesquisarregistro</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Ação de macro ClearMacroError</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="onerror-macro-action.md">Ação de macro OnError</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="raiseerror-macro-action.md">Ação de macro RaiseError</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="setlocalvar-macro-action.md">Ação de macro SetLocalVar</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="stopmacro-macro-action.md">Ação de macro StopMacro</a></p></td>
</tr>
</tbody>
</table>


Para criar uma Macro de Dados que capture o evento **Antes de Excluir**, siga estas etapas.

1.  Abra a tabela na qual deseja capturar o evento **Antes de Excluir**.

2.  Na guia **tabela** , no grupo **Antes de eventos** , selecione **Antes de excluir**.

