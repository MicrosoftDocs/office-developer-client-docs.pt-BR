---
title: Ação da macro DefinirVariávelTemporária
TOCTitle: SetTempVar macro action
ms:assetid: 9c3b7bee-02c5-efbf-1276-4c4a1f7802d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198102(v=office.15)
ms:contentKeyID: 48546593
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm150219
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b630304774e521162687d4c78a6a97cf18ddb419
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705223"
---
# <a name="settempvar-macro-action"></a>Ação da macro DefinirVariávelTemporária


**Aplica-se a**: Access 2013, o Office 2013



Use a ação **DefinirVariávelTemporária** para criar uma variável temporária e defini-la com um valor específico. A variável poderá ser usada como condição ou argumento em ações subsequentes, ou em outra macro, em um procedimento de evento, ou ainda em um formulário ou relatório.

## <a name="setting"></a>Configuração

A ação **DefinirVariávelTemporária** tem os seguintes argumentos.

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
<td><p><strong>Name</strong></p></td>
<td><p>Digite o nome da variável temporária.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expressão</strong>.</p></td>
<td><p>Insira uma expressão que será usada para definir o valor dessa variável temporária. Não preceda a expressão com igual (<strong>=</strong>) entrada. Você pode clicar no botão <strong>Construir</strong> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> para usar o Construtor de Expressões para definir este argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

- É possível definir até 255 variáveis temporárias de uma só vez. Se você não remover uma variável temporária, ela permanecerá na memória até você fechar o banco de dados. É recomendável remover variáveis temporárias após a conclusão do trabalho. Para remover uma única variável temporária, use a ação **[RemoverVariávelTemporária](removetempvar-macro-action.md)** e defina o respectivo argumento com o nome da variável temporária a ser removida. Se for necessário remover mais de uma variável temporária e você quiser removê-las todas de uma só vez, use a ação **RemoverTodasVariáveisTemporárias**.

- Variáveis temporária são globais. Após a criação de uma variável temporária, você pode referenciá-la em um procedimento de evento, um módulo do VBA (Visual Basic for Applications), uma consulta ou em uma expressão. Por exemplo, se você criou uma variável temporária chamada *MINHAVARIÁVEL*, você poderia usar a variável como a fonte de controle para uma caixa de texto usando a seguinte sintaxe:
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > [!OBSERVAçãO] Em macros, consultas e procedimentos de evento, não é preciso preceder a expressão com um sinal de igualdade.
 
  Também é possível referenciar variáveis temporárias em qualquer suplemento ou bancos de dados especificado.

- Para executar a ação **DefinirVariávelTemporária** em um módulo do VBA, use o método **Add** do objeto **TempVars**.

## <a name="example"></a>Exemplo

A macro a seguir demonstra como criar uma variável temporária usando a ação **DefinirVariávelTemporária** e, depois, utilizando-a em uma condição e em uma caixa de mensagem, e finalmente removendo-a.

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
<td><p><strong>Definirvariáveltemporária</strong></p></td>
<td><p><strong>Nome</strong>: MINHAVARIÁVEL<strong>expressão</strong>: CaixaDeEntrada (&quot;Insira um número diferente de zero.&quot;)</p></td>
</tr>
<tr class="even">
<td><p>[Varstemp]! [MINHAVARIÁVEL] &lt; &gt;0</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: =&quot;você digitou &quot; &amp; [Varstemp]! [MINHAVARIÁVEL] &amp; &quot;. &quot; <strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>informações</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Removervariáveltemporária</strong></p></td>
<td><p><strong>Nome</strong>: MinhaVar</p></td>
</tr>
</tbody>
</table>

