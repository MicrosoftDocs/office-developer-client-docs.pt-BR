---
title: Ação de macro IrParaPágina
TOCTitle: GoToPage Macro Action
ms:assetid: 611aadff-83b7-e74d-4093-93fb5ce6e3ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194858(v=office.15)
ms:contentKeyID: 48545199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm129285
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dc7777535fdba5bcb1f6ace167e23e1294f13960
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462909"
---
# <a name="gotopage-macro-action"></a>Ação de macro IrParaPágina


**Aplica-se a**: Access 2013 | Office 2013

Você pode usar a ação **IrParaPágina** para mover o foco no formulário ativo para o primeiro controle em uma página especificada. É possível usar esta ação se você criou um formulário com quebras de páginas que contém grupos de informações relacionadas. Por exemplo, talvez haja um formulário Funcionários com informações pessoais em uma página, informações de escritório em outra e informações de vendas em uma terceira página. Você pode usar a ação **IrParaPágina** para se mover para a página desejada. Também pode apresentar várias páginas de informações em um único formulário usando controles guia.

## <a name="setting"></a>Configuração

A ação **IrParaPágina** tem os seguintes argumentos.

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
<td><p><strong>Número de página</strong></p></td>
<td><p>O número da página para a qual você deseja mover o foco. Insira o número de página na caixa <strong>Número de Página</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Se você deixar este argumento em branco, o foco continuará na página atual. É possível usar os argumentos <strong>À Direita</strong> e <strong>Abaixo</strong> para exibir a parte da página que deseja ver.</p></td>
</tr>
<tr class="even">
<td><p><strong>Right</strong></p></td>
<td><p>A posição horizontal do local da página, medida a partir da borda esquerda da janela que a contém, que aparecerá na borda esquerda da janela. Ela será obrigatória se você especificar um argumento <strong>Abaixo</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Down</strong></p></td>
<td><p>A posição vertical do local da página, medida a partir da borda superior da janela que a contém, que aparecerá na borda superior da janela. Ela será obrigatória se você especificar um argumento <strong>À Direita</strong>.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>[!OBSERVAçãO] Os argumentos <STRONG>À Direita</STRONG> e <STRONG>Abaixo</STRONG> são medidos em polegadas ou centímetros, dependendo das configurações regionais do Painel de Controle do Windows.</P>



## <a name="remarks"></a>Comentários

Você pode usar esta ação para selecionar o primeiro controle (conforme definido pela ordem de tabulação do formulário) na página especificada. Use a ação **IrParaControle** para se mover para um controle específico no formulário.

Você pode usar os argumentos **direita** e **para baixo** para formulários com páginas maiores que a janela do Access. Use o argumento **Número de Página** para se mover para a página desejada e use os argumentos **À Direita** e **Abaixo** para exibir a parte da página que deseja ver. O Access exibe a parte da página cujo canto superior esquerdo está deslocado na distância especificada a partir do canto superior esquerdo da página.

Não use a ação **IrParaPágina** nos seguintes casos:

  - Para mover o foco para uma página em um formulário oculto.

  - Para mover o foco de uma página para outra em um controle guia.

Para executar a ação **IrParaPágina** em um módulo do VBA (Visual Basic for Applications), use o método **GoToPage** do objeto **DoCmd**.
