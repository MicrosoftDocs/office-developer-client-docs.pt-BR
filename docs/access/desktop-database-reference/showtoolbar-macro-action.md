---
title: Ação da macro MostrarBarraDeFerramentas
TOCTitle: ShowToolbar macro action
ms:assetid: 9e53009b-1e5e-1bee-3bcc-f82dc1b0dc48
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198288(v=office.15)
ms:contentKeyID: 48546649
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm27417
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 01ba59ce0898068788adb9269b3203794d1f31d4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700336"
---
# <a name="showtoolbar-macro-action"></a>Ação da macro MostrarBarraDeFerramentas

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **MostrarBarraDeFerramentas** para exibir ou ocultar um grupo de comandos na guia **Suplementos**.

> [!NOTE]
> - [!OBSERVAçãO] A ação **MostrarBarraDeFerramentas** não afeta os menus de atalho.
> - [!OBSERVAçãO] This action will not be allowed if the database is not trusted. 

## <a name="setting"></a>Configuração

A ação **MostrarBarraDeFerramentas** tem os seguintes argumentos.

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
<td><p><strong>Nome da barra de ferramentas</strong></p></td>
<td><p>O nome do grupo de comando na guia <strong>Suplementos</strong> que você deseja exibir ou ocultar. A caixa <strong>Nome da barra de ferramentas</strong> na seção <strong>Argumentos da ação</strong> do painel do construtor de Macro mostra todos os grupos disponíveis que podem ser afetados por essa ação. Este é um argumento obrigatório. Se você executar uma macro contendo a ação <strong>MostrarBarraDeFerramentas</strong> em um banco de dados biblioteca, o Access pesquisará o grupo com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>Show</strong></p></td>
<td><p>Especifica para exibir ou ocultar o grupo e em quais modos de exibição para exibir ou ocultar a ele. O padrão é <strong>Sim</strong> (Mostrar grupo sempre). Você pode selecionar <strong>Sim</strong> para exibir o grupo em todos os horários, <strong>Onde apropriado</strong> para exibir o grupo somente quando o formulário apropriado ou relatório estiver ativo, ou <strong>não</strong> para ocultar o grupo em todas as ocasiões.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Esta ação pode ser usada em uma macro com expressões condicionais para exibir ou ocultar um grupo, dependendo de certas condições.

Se você quiser mostrar um determinado grupo em apenas um formulário ou relatório, defina a propriedade **AoAtivar** do formulário ou do relatório usando o nome de uma macro que contenha uma ação **MostrarBarraDeFerramentas** para mostrar o grupo. Depois defina a propriedade **AoDesativar** do formulário ou do relatório usando o nome de uma macro que contenha a ação **MostrarBarraDeFerramentas** para ocultar o grupo.

Não será possível exibir ou ocultar barras de ferramentas internas se a propriedade **AllowBuiltInToolbars** for definida como **False** (0) em um módulo do VBA (Visual Basic for Applications) ou se a opção **Allow Built-in Toolbars** for definida como **False** no VBA com o método **SetOption**.

Para executar a ação **MostrarBarraDeFerramentas** em um módulo do VBA, use o método **ShowToolbar** do objeto **DoCmd**.

