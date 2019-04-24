---
title: Ação da macro LimparErrodeMacro
TOCTitle: ClearMacroError macro action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f42386674ff76d550fb47a971860b4e1a5905236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296371"
---
# <a name="clearmacroerror-macro-action"></a>Ação da macro LimparErrodeMacro


**Aplica-se ao:** Access 2013, Office 2013


Você pode usar a ação **LimparErrodeMacro** para limpar as informações sobre um erro armazenado no objeto **MacroError**.

## <a name="setting"></a>Configuração

A ação **LimparErrodeMacro** não tem nenhum argumento.

## <a name="remarks"></a>Comentários

- Quando ocorre um erro em uma macro, informações sobre o erro são armazenadas no objeto **MacroError**. Se você não tiver usado a ação **[AoOcorrerErro](onerror-macro-action.md)** para suprimir mensagens de erro, a macro será interrompida e as informações de erro serão exibidas em uma mensagem de erro padrão. No enTanto, se você tiver usado a ação **AoOcorrerErro** para suprimir mensagens de erro, talvez queira usar as informações armazenadas no objeto **MacroError** em uma condição ou em uma mensagem de erro personalizada.
    
  Depois que um erro for manipulado, as informações do objeto **MacroError** estarão desatualizadas, portanto é uma ótima ideia limpar o objeto usando a ação **LimparErrodeMacro**. Esse procedimento redefinirá o número de erro no objeto **MacroError** como 0 e limpará todas as outras informações sobre o erro armazenado no objeto, como descrição do erro, nome da macro, nome da ação, condição e argumentos. Dessa maneira, você poderá inspecionar o objeto **MacroError** outra vez mais tarde para saber se ocorreu outro erro.

- O objeto **MacroError** é limpo automaticamente quando qualquer macro chega ao fim, por isso não é necessário usar a ação **LimparErrodeMacro** no fim de uma macro.

- O objeto **MacroError** contém informações somente sobre um erro de cada vez. Se ocorrer mais de um erro em uma macro, o objeto **MacroError** conterá informações somente sobre o último erro.

- Para executar a ação **LimparErrodeMacro** em um módulo do VBA, use o método **ClearMacroError** do objeto **DoCmd**.

## <a name="example"></a>Exemplo

A macro a seguir usa a ação **AoOcorrerErro** com o argumento **Próximo** para suprimir mensagens de erro, além de usar a ação **AbrirFormulário** para abrir um formulário. Para este exemplo, um erro é criado deliberadamente usando a ação **IrParaRegistro** para ir até o registro anterior. A condição ** \[MacroError\].\[ O\]\<número\>0** testa o objeto **MacroError** . Se um erro tiver ocorrido, o número do erro será diferente de zero, e a ação **CaixadeMensagem** será executada. A caixa de mensagem exibirá o nome da ação que causou o erro (nesse caso, a ação **IrParaRegistro** ) e o número do erro será exibido. Por fim, a execução da ação **LimparErrodeMacro** limpa o objeto **ErrodeMacro**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condição</p></th>
<th><p>Ação</p></th>
<th><p>Argumentos</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OnError</strong></p></td>
<td><p><strong>Ir para</strong>: <strong>Próximo</strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nome do formulário</strong>:<strong>modo de exibição</strong>formuláriodacategoria: <strong>modo FormWindow</strong>: <strong>normal</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToRecord</strong></p></td>
<td><p><strong>Tipo de objeto</strong>: <strong>nome</strong>do formObject:<strong>registro</strong>formuláriodacategoria: anterior</p></td>
</tr>
<tr class="even">
<td><p>[MacroError]. Série &lt; &gt;0</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: =&quot;erro # &quot; &amp; [MacroError]. Série &amp; em &quot; [ &amp; MacroError]. &quot; ActionName &amp; &quot; ação. &quot; <strong>Aviso sonoro</strong>: <strong>YesType</strong>: informações</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>ClearMacroError</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

