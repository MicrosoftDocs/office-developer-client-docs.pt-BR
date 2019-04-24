---
title: Ação da macro ExecutarComandodeMenu
TOCTitle: RunMenuCommand macro action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c2b5a19b7a92fb68dfb774afeec5cd6ba456f38d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306500"
---
# <a name="runmenucommand-macro-action"></a>Ação da macro ExecutarComandodeMenu

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **ExecutarComandodeMenu** para executar um comando interno do Microsoft Access.

## <a name="setting"></a>Configuração

A ação **ExecutarComandodeMenu** tem o argumento de ação a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Command</strong></p></td>
<td><p>O nome do comando a ser executado. A caixa <strong>Comando</strong> mostra os comandos internos disponíveis no Access, em ordem alfabética. Este é um argumento obrigatório.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentários

Você pode usar a ação **ExecutarComandodeMenu** para executar um comando do Access em uma barra de menus personalizada, na barra de menus global, em um menu de atalho personalizado ou no menu de atalho global.

Use a ação **ExecutarComandodeMenu** em uma macro com expressões condicionais para executar um comando que dependa de certas condições.

> [!NOTE]
> [!OBSERVAçãO] Se você clicar na guia **Arquivo** e depois clicar em **Recente**, isso mostrará os bancos de dados usados mais recentemente. Você pode clicar em um desses bancos de dados em vez de clicar em **Abrir**. Esses itens de banco de dados não são exibidos na caixa de listagem suspensa do argumento **Comando** e não estão disponíveis quando a ação **ExecutarComandodeMenu** é usada em uma macro.

Quando você converte um banco de dados do Access de uma versão anterior, alguns comandos talvez não fiquem mais disponíveis. Um comando pode ser renomeado, movido para outro menu ou deixar de estar disponível no Access. Não é possível converter as ações **ExecutarItemdoMenu** desses comandos em ações **ExecutarComandodeMenu**. Quando você abrir a macro, o Access exibirá uma ação **ExecutarComandodeMenu** com um argumento **Comando** em branco para esses argumentos. É preciso editar a macro e inserir um argumento de comando válido ou então excluir a ação **ExecutarComandodeMenu**.

Para executar a ação **ExecutarComandodeMenu** em um módulo do VBA(Visual Basic for Applications), use o método **ExecutarComando** do objeto **Application** (isso equivale ao método **ExecutarComando** do objeto **DoCmd** ).

