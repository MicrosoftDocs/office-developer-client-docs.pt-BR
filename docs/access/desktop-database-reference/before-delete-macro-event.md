---
title: Evento da macro Antes da Exclusão
TOCTitle: Before Delete macro event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2b2a4f978a4af2ba79cab7807f0142d35d7d30c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296910"
---
# <a name="before-delete-macro-event"></a>Evento da macro Antes da Exclusão

**Aplica-se ao:** Access 2013, Office 2013

O evento **Antes de Excluir** ocorre quando um registro é excluído, mas antes da alteração ser submetida.

> [!NOTE]
> O evento **Antes de Excluir** está disponível somente em Macros de Dados.

## <a name="remarks"></a>Comentários

Use o evento **Antes de Excluir** para executar qualquer ação que você deseja que ocorra antes da exclusão de um registro. O **Antes de Alterar** é comumente usado para executar validação e criar mensagens de erro personalizadas.

Você pode acessar um valor no registro a ser excluído usando a seguinte sintaxe:

`[Old].[Field Name]`

Por exemplo, para acessar o valor do campo Quantidadeemestoque no registro a ser excluído, use a seguinte sintaxe:

`[Old].[QuantityInStock]`

Os valores contidos no registro a ser excluído são excluídos permanentemente após a conclusão do evento **Antes de Excluir**.

Você pode cancelar o evento **Antes de Excluir** utilizando a ação **GerarErro**. Quando um erro é gerado, as alterações contidas no evento **antes de excluir** são descartadas.

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
<td><p><a href="comment-macro-statement.md">Instrução de macro Comentário</a></p></td>
</tr>
<tr class="even">
<td><p>Fluxo do programa</p></td>
<td><p><a href="group-macro-statement.md">Instrução de macro Grupo</a></p></td>
</tr>
<tr class="odd">
<td><p>Fluxo do programa</p></td>
<td><p><a href="if-then-else-macro-block.md">Bloco de macro If...Then...Else</a></p></td>
</tr>
<tr class="even">
<td><p>Bloco de dados</p></td>
<td><p><a href="lookuprecord-data-block.md">Ação de macro Pesquisarregistro</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Ação da macro LimparErrodeMacro</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="onerror-macro-action.md">Ação da macro AoOcorrerErro</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="raiseerror-macro-action.md">Ação da macro GerarErro</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="setlocalvar-macro-action.md">Ação da macro DefinirVarLocal</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="stopmacro-macro-action.md">Ação da macro PararMacro</a></p></td>
</tr>
</tbody>
</table>


Para criar uma Macro de Dados que capture o evento **Antes de Excluir**, siga estas etapas.

1.  Abra a tabela na qual deseja capturar o evento **Antes de Excluir**.

2.  Na guia **tabela** , no grupo **antes de eventos** , selecione **antes de excluir**.

