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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306472"
---
# <a name="showtoolbar-macro-action"></a>Ação da macro MostrarBarraDeFerramentas

**Aplica-se ao:** Access 2013, Office 2013

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
<td><p>O nome do grupo de comandos na guia <strong>Suplementos</strong> a ser exibido ou ocultado. A caixa <strong>Nome da Barra de Ferramentas</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros mostra todos os grupos disponíveis e que possam ser afetados por esta ação. Este é um argumento obrigatório. Se você executar uma macro contendo a ação <strong>MostrarBarraDeFerramentas</strong> em um banco de dados biblioteca, o Access pesquisará o grupo com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>Show</strong></p></td>
<td><p>Especifica se o grupo deve ser exibido ou ocultado e em quais modos de exibição isso ocorrerá. O padrão é <strong>Sim</strong> (sempre mostrar o grupo). Você pode selecionar <strong>Sim</strong> para exibir o grupo em todos os momentos, <strong>onde apropriado</strong> para exibir o grupo somente quando o formulário ou relatório apropriado estiver ativo, ou <strong>não</strong> para ocultar o grupo o tempo todo.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Esta ação pode ser usada em uma macro com expressões condicionais para exibir ou ocultar um grupo, dependendo de certas condições.

Se você quiser mostrar um determinado grupo em apenas um formulário ou relatório, defina a propriedade **AoAtivar** do formulário ou do relatório usando o nome de uma macro que contenha uma ação **MostrarBarraDeFerramentas** para mostrar o grupo. Depois defina a propriedade **AoDesativar** do formulário ou do relatório usando o nome de uma macro que contenha a ação **MostrarBarraDeFerramentas** para ocultar o grupo.

Não será possível exibir ou ocultar barras de ferramentas internas se a propriedade **AllowBuiltInToolbars** for definida como **False** (0) em um módulo do VBA (Visual Basic for Applications) ou se a opção **Allow Built-in Toolbars** for definida como **False** no VBA com o método **SetOption**.

Para executar a ação **MostrarBarraDeFerramentas** em um módulo do VBA, use o método **ShowToolbar** do objeto **DoCmd**.

