---
title: Ação da macro AdicionarMenu
TOCTitle: AddMenu macro action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d04c98da0ecef1c2323930c74588b7a6a07c2e29
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026264"
---
# <a name="addmenu-macro-action"></a>Ação da macro AdicionarMenu


**Aplica-se a**: Access 2013, o Office 2013

Este artigo descreve a operação básica da ação de macro **AdicionarMenu**.

Use a ação **AdicionarMenu** para criar:

- Menus personalizados na guia **Suplementos** de um formulário ou relatório específico.

- Um menu de atalho personalizado de um formulário, relatório ou controle. O menu de atalho personalizado substitui o menu de atalho interno do formulário, relatório ou controle.

- Um menu de atalho global. O menu de atalho global substitui o menu de atalho interno de campos em folhas de dados de consulta e tabela, formulários e relatórios, com exceção de onde foi adicionado um menu de atalho personalizado de um formulário, relatório ou controle.

## <a name="setting"></a>Configuração

A ação **AdicionarMenu** tem os seguintes argumentos.

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
<td><p><strong>Nome do Menu</strong></p></td>
<td><p>O nome do menu, por exemplo, &quot;comandos do relatório&quot; ou &quot;ferramentas&quot;. Para criar uma tecla de acesso para que você pode usar o teclado para escolher o menu, digite um e comercial (<strong>&amp;</strong>) antes da letra que farão parte a tecla de acesso. Essa letra será sublinhada no nome do menu na guia <strong>Suplementos</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>Nome da Macro do Menu</strong></p></td>
<td><p>O nome do grupo de macros que contém as macros dos comandos do menu. Esse é um argumento obrigatório. 

</p>
<p><strong>Observação</strong>: se você executar uma macro que contém a ação <strong>AdicionarMenu</strong> em um banco de dados biblioteca, Microsoft Office Access 2007 procurará o grupo de macros com esse nome de banco de dados atual.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Texto da Barra de Status</strong></p></td>
<td><p>O texto que será exibido na barra de status quando o menu for selecionado. Este argumento é ignorado para menus de atalho.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Para executar a ação **AdicionarMenu** em um módulo do VBA (Visual Basic for Applications), use o método **AddMenu** do objeto **DoCmd**. Você também pode definir a propriedade **BarraDeMenu** ou **ShortcutMenuBar** do VBA para criar um menu personalizado na guia **Suplementos** ou anexar um menu de atalho personalizado a um formulário, relatório ou controle. Defina a propriedade **ShortcutMenuBar** do objeto **Application** para criar um menu de atalho global.

