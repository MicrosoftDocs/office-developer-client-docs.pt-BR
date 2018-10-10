---
title: Ação da macro ExecutarMacro
TOCTitle: RunMacro Macro Action
ms:assetid: 25966f20-8160-0821-b88a-ed08b7786fdc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191868(v=office.15)
ms:contentKeyID: 48543787
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm43195
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 533ac6aff194296a9e4470e01672a8338dcbc318
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465076"
---
# <a name="runmacro-macro-action"></a>Ação da macro ExecutarMacro


**Aplica-se a**: Access 2013 | Office 2013

Você pode usar a ação **ExecutarMacro** para executar uma macro. A macro pode estar em um grupo de macros.

Você pode usar a ação:

  - Para executar uma macro em outra macro.

  - Executar uma macro baseada em uma determinada condição.

  - Anexar uma macro a um comando de menu personalizado.

## <a name="setting"></a>Configuração

A ação **ExecutarMacro** tem os argumentos a seguir.

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
<td><p><strong>Nome da Macro</strong></p></td>
<td><p>O nome da macro a ser executada. Caixa <strong>Nome da Macro</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros mostra todas as macros (e grupos de macro) no banco de dados atual. Se a macro estiver em um grupo de macros, ela é listada sob o nome do grupo de macros na lista como <em>nomedogrupodemacros</em>. <em>macroname</em>. Este é um argumento obrigatório. Se você executar uma macro contendo a ação <strong>ExecutarMacro</strong> em um banco de dados biblioteca, o Microsoft Access pesquisará a macro com esse nome no banco de dados biblioteca, e não no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>Contagem de repetição</strong></p></td>
<td><p>O número máximo de vezes que a macro será executada. Se você deixar este argumento em branco (e o argumento <strong>Expressão de repetição</strong> também estiver em branco), a macro será executada uma única vez.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Expressão de repetição</strong></p></td>
<td><p>Uma expressão que avalia se <strong>True</strong> (–1) ou <strong>False</strong> (0). A execução da macro será interrompida se a expressão avaliar como <strong>False</strong>. A expressão é avaliada sempre que a macro é executada.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Se você inserir um nome de grupo de macros para o argumento **Nome da macro**, o Access executará a primeira macro do grupo.

Esta ação é semelhante a clicar em **Executar Macro** na guia **Ferramentas de Banco de Dados**, selecionar uma macro e clicar em **OK**. Entretanto, esse comando executa a macro uma única vez, ao passo que a ação **ExecutarMacro** pode executar uma macro quantas vezes você quiser.


> [!TIP]
> <P>[!DICA] Use os argumentos <STRONG>Contagem de repetição</STRONG> e <STRONG>Expressão de repetição</STRONG> para determinar quantas vezes a macro deve ser executada:</P>



  - Se você deixar os dois argumentos em branco, a macro será executada uma única vez.

  - Se você inserir um número em **Contagem de repetição**, mas deixar **Expressão de repetição** em branco, a macro será executada pelo número de vezes especificado.

  - Se você deixar **Contagem de repetição** em branco, mas inserir uma expressão em **Expressão de repetição**, a macro será executada até que a expressão avalie como **False**.

  - Se você inserir valores para os dois argumentos, a macro será executada pelo número de vezes especificado em **Contagem de repetição** ou até que **Expressão de repetição** avalie como **False**, o que ocorrer primeiro.

Se uma macro contendo a ação **ExecutarMacro** for executada e ela alcançar a ação **ExecutarMacro**, o Access executará a macro chamada. Após a conclusão da macro chamada, o Access retornará à macro original e executará a próxima ação.


> [!NOTE]
> <UL>
> <LI>
> <P>É possível chamar uma macro do mesmo grupo de macros ou de outro grupo.</P>
> <LI>
> <P>Você pode aninhar macros. Ou seja, você pode executar a macro A que, por sua vez, chama a macro B etc. Em cada caso, quando a macro chamada é concluída, o Access retorna à macro que a chamou e executa a próxima ação dessa macro.</P></LI></UL>



Para executar a ação **ExecutarMacro** em um módulo do VBA(Visual Basic for Applications), use o método **RunMacro** do objeto **DoCmd**.

