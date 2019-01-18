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
# <a name="settempvar-macro-action"></a><span data-ttu-id="fdfa0-102">Ação da macro DefinirVariávelTemporária</span><span class="sxs-lookup"><span data-stu-id="fdfa0-102">SetTempVar macro action</span></span>


<span data-ttu-id="fdfa0-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fdfa0-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="fdfa0-p101">Use a ação **DefinirVariávelTemporária** para criar uma variável temporária e defini-la com um valor específico. A variável poderá ser usada como condição ou argumento em ações subsequentes, ou em outra macro, em um procedimento de evento, ou ainda em um formulário ou relatório.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-p101">You can use the **SetTempVar** action to create a temporary variable and set it to a specific value. The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another macro, in an event procedure, or on a form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="fdfa0-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="fdfa0-106">Setting</span></span>

<span data-ttu-id="fdfa0-107">A ação **DefinirVariávelTemporária** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-107">The **SetTempVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fdfa0-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="fdfa0-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="fdfa0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="fdfa0-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fdfa0-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="fdfa0-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="fdfa0-111">Digite o nome da variável temporária.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-111">Enter the name of the temporary variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdfa0-112"><strong>Expressão</strong>.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-112"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="fdfa0-113">Insira uma expressão que será usada para definir o valor dessa variável temporária.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-113">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="fdfa0-114">Não preceda a expressão com igual (<strong>=</strong>) entrada.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-114">Do not precede the expression with the equal (<strong>=</strong>) sign.</span></span> <span data-ttu-id="fdfa0-115">Você pode clicar no botão <strong>Construir</strong></span><span class="sxs-lookup"><span data-stu-id="fdfa0-115">You can click the <strong>Build</strong> button</span></span> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> <span data-ttu-id="fdfa0-117">para usar o Construtor de Expressões para definir este argumento.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-117">to use the Expression Builder to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fdfa0-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdfa0-118">Remarks</span></span>

- <span data-ttu-id="fdfa0-p103">É possível definir até 255 variáveis temporárias de uma só vez. Se você não remover uma variável temporária, ela permanecerá na memória até você fechar o banco de dados. É recomendável remover variáveis temporárias após a conclusão do trabalho. Para remover uma única variável temporária, use a ação **[RemoverVariávelTemporária](removetempvar-macro-action.md)** e defina o respectivo argumento com o nome da variável temporária a ser removida. Se for necessário remover mais de uma variável temporária e você quiser removê-las todas de uma só vez, use a ação **RemoverTodasVariáveisTemporárias**.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-p103">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database. It is a good practice to remove temporary variables when you are finished using them. To remove a single temporary variable, use the **[RemoveTempVar](removetempvar-macro-action.md)** action and set its argument to the name of the temporary variable that you want to remove. If you have more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

- <span data-ttu-id="fdfa0-124">Variáveis temporária são globais.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-124">Temporary variables are global.</span></span> <span data-ttu-id="fdfa0-125">Após a criação de uma variável temporária, você pode referenciá-la em um procedimento de evento, um módulo do VBA (Visual Basic for Applications), uma consulta ou em uma expressão.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-125">Once a temporary variable has been created, you can refer to it in an event procedure, a Visual Basic for Applications (VBA) module, a query, or an expression.</span></span> <span data-ttu-id="fdfa0-126">Por exemplo, se você criou uma variável temporária chamada *MINHAVARIÁVEL*, você poderia usar a variável como a fonte de controle para uma caixa de texto usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="fdfa0-126">For example, if you created a temporary variable named *MyVar*, you could use the variable as the control source for a text box by using the following syntax:</span></span>
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > <span data-ttu-id="fdfa0-127">[!OBSERVAçãO] Em macros, consultas e procedimentos de evento, não é preciso preceder a expressão com um sinal de igualdade.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-127">In macros, queries and event procedures, you do not need to precede the expression with an equal sign.</span></span>
 
  <span data-ttu-id="fdfa0-128">Também é possível referenciar variáveis temporárias em qualquer suplemento ou bancos de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-128">You can also refer to temporary variables in any add-ins or referenced databases.</span></span>

- <span data-ttu-id="fdfa0-129">Para executar a ação **DefinirVariávelTemporária** em um módulo do VBA, use o método **Add** do objeto **TempVars**.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-129">To run the **SetTempVar** action in a VBA module, use the **Add** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="fdfa0-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fdfa0-130">Example</span></span>

<span data-ttu-id="fdfa0-131">A macro a seguir demonstra como criar uma variável temporária usando a ação **DefinirVariávelTemporária** e, depois, utilizando-a em uma condição e em uma caixa de mensagem, e finalmente removendo-a.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-131">The following macro demonstrates how to create a temporary variable by using the **SetTempVar** action, then using the temporary variable in a condition and a message box, and then removing the temporary variable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fdfa0-132">Condição</span><span class="sxs-lookup"><span data-stu-id="fdfa0-132">Condition</span></span></p></th>
<th><p><span data-ttu-id="fdfa0-133">Ação</span><span class="sxs-lookup"><span data-stu-id="fdfa0-133">Action</span></span></p></th>
<th><p><span data-ttu-id="fdfa0-134">Argumentos</span><span class="sxs-lookup"><span data-stu-id="fdfa0-134">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="fdfa0-135"><strong>Definirvariáveltemporária</strong></span><span class="sxs-lookup"><span data-stu-id="fdfa0-135"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="fdfa0-136"><strong>Nome</strong>: MINHAVARIÁVEL<strong>expressão</strong>: CaixaDeEntrada (&quot;Insira um número diferente de zero.&quot;)</span><span class="sxs-lookup"><span data-stu-id="fdfa0-136"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdfa0-137">[Varstemp]! [MINHAVARIÁVEL] &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="fdfa0-137">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="fdfa0-138"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="fdfa0-138"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="fdfa0-139"><strong>Mensagem</strong>: =&quot;você digitou &quot; &amp; [Varstemp]! [MINHAVARIÁVEL] &amp; &quot;. &quot; <strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>informações</strong></span><span class="sxs-lookup"><span data-stu-id="fdfa0-139"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="fdfa0-140"><strong>Removervariáveltemporária</strong></span><span class="sxs-lookup"><span data-stu-id="fdfa0-140"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="fdfa0-141"><strong>Nome</strong>: MinhaVar</span><span class="sxs-lookup"><span data-stu-id="fdfa0-141"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

