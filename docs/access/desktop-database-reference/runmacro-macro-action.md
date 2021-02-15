---
title: Ação da macro ExecutarMacro
TOCTitle: RunMacro macro action
ms:assetid: 25966f20-8160-0821-b88a-ed08b7786fdc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191868(v=office.15)
ms:contentKeyID: 48543787
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm43195
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d9e86fb7d60af94d6ecde71b2a857a3cc5b9bcb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306850"
---
# <a name="runmacro-macro-action"></a><span data-ttu-id="f2959-102">Ação da macro ExecutarMacro</span><span class="sxs-lookup"><span data-stu-id="f2959-102">RunMacro macro action</span></span>

<span data-ttu-id="f2959-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2959-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f2959-p101">Você pode usar a ação **ExecutarMacro** para executar uma macro. A macro pode estar em um grupo de macros.</span><span class="sxs-lookup"><span data-stu-id="f2959-p101">You can use the **RunMacro** action to run a macro. The macro can be in a macro group.</span></span>

<span data-ttu-id="f2959-106">Você pode usar a ação:</span><span class="sxs-lookup"><span data-stu-id="f2959-106">You can use this action:</span></span>

- <span data-ttu-id="f2959-107">Para executar uma macro em outra macro.</span><span class="sxs-lookup"><span data-stu-id="f2959-107">To run a macro from within another macro.</span></span>

- <span data-ttu-id="f2959-108">Executar uma macro baseada em uma determinada condição.</span><span class="sxs-lookup"><span data-stu-id="f2959-108">To run a macro based on a certain condition.</span></span>

- <span data-ttu-id="f2959-109">Anexar uma macro a um comando de menu personalizado.</span><span class="sxs-lookup"><span data-stu-id="f2959-109">To attach a macro to a custom menu command.</span></span>

## <a name="setting"></a><span data-ttu-id="f2959-110">Setting</span><span class="sxs-lookup"><span data-stu-id="f2959-110">Setting</span></span>

<span data-ttu-id="f2959-111">A ação **ExecutarMacro** tem os argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2959-111">The **RunMacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2959-112">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="f2959-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f2959-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2959-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2959-114"><strong>Nome da Macro</strong></span><span class="sxs-lookup"><span data-stu-id="f2959-114"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f2959-115">O nome da macro a ser executada.</span><span class="sxs-lookup"><span data-stu-id="f2959-115">The name of the macro to run.</span></span> <span data-ttu-id="f2959-116">A <strong>caixa Nome da</strong> Macro na seção <strong>Argumentos</strong> da Ação do painel Construtor de Macros mostra todas as macros (e grupos de macros) no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="f2959-116">The <strong>Macro Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all macros (and macro groups) in the current database.</span></span> <span data-ttu-id="f2959-117">Se a macro estiver em um grupo de macros, ela será listada sob o nome do grupo de macros na lista como <em>nome do grupo de macros.</em> <em>macroname</em>.</span><span class="sxs-lookup"><span data-stu-id="f2959-117">If the macro is in a macro group, it's listed under the macro group name in the list as <em>macrogroupname</em>.<em>macroname</em>.</span></span> <span data-ttu-id="f2959-118">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f2959-118">This is a required argument.</span></span> <span data-ttu-id="f2959-119">Se você executar uma macro contendo a ação <strong>ExecutarMacro</strong> em um banco de dados biblioteca, o Microsoft Access pesquisará a macro com esse nome no banco de dados biblioteca, e não no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="f2959-119">If you run a macro containing the <strong>RunMacro</strong> action in a library database, Microsoft Access looks for the macro with this name in the library database and doesn't look for it in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2959-120"><strong>Contagem de repetição</strong></span><span class="sxs-lookup"><span data-stu-id="f2959-120"><strong>Repeat Count</strong></span></span></p></td>
<td><p><span data-ttu-id="f2959-p103">O número máximo de vezes que a macro será executada. Se você deixar este argumento em branco (e o argumento <strong>Expressão de repetição</strong> também estiver em branco), a macro será executada uma única vez.</span><span class="sxs-lookup"><span data-stu-id="f2959-p103">The maximum number of times the macro will run. If you leave this argument blank (and the <strong>Repeat Expression</strong> argument is also blank), the macro runs once.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2959-123"><strong>Expressão de repetição</strong></span><span class="sxs-lookup"><span data-stu-id="f2959-123"><strong>Repeat Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="f2959-p104">Uma expressão que avalia se <strong>True</strong> (–1) ou <strong>False</strong> (0). A execução da macro será interrompida se a expressão avaliar como <strong>False</strong>. A expressão é avaliada sempre que a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="f2959-p104">An expression that evaluates to <strong>True</strong> (–1) or <strong>False</strong> (0). The macro stops running if the expression evaluates to <strong>False</strong>. The expression is evaluated each time the macro runs.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="f2959-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2959-127">Remarks</span></span>

<span data-ttu-id="f2959-128">Se você inserir um nome de grupo de macros para o argumento **Nome da macro**, o Access executará a primeira macro do grupo.</span><span class="sxs-lookup"><span data-stu-id="f2959-128">If you enter a macro group name for the **Macro Name** argument, Access runs the first macro in the macro group.</span></span>

<span data-ttu-id="f2959-p105">Esta ação é semelhante a clicar em **Executar Macro** na guia **Ferramentas de Banco de Dados**, selecionar uma macro e clicar em **OK**. Entretanto, esse comando executa a macro uma única vez, ao passo que a ação **ExecutarMacro** pode executar uma macro quantas vezes você quiser.</span><span class="sxs-lookup"><span data-stu-id="f2959-p105">This action is similar to clicking **Run Macro** on the **Database Tools** tab, selecting a macro, and clicking **OK**. However, this command runs the macro only once, whereas the **RunMacro** action can run a macro as many times as you want.</span></span>

> [!TIP]
> <span data-ttu-id="f2959-131">[!DICA] Use os argumentos **Contagem de repetição** e **Expressão de repetição** para determinar quantas vezes a macro deve ser executada:</span><span class="sxs-lookup"><span data-stu-id="f2959-131">You can use the **Repeat Count** and **Repeat Expression** arguments to determine how many times the macro runs:</span></span>
> - <span data-ttu-id="f2959-132">Se você deixar os dois argumentos em branco, a macro será executada uma única vez.</span><span class="sxs-lookup"><span data-stu-id="f2959-132">If you leave both arguments blank, the macro runs once.</span></span>
> - <span data-ttu-id="f2959-133">Se você inserir um número em **Contagem de repetição**, mas deixar **Expressão de repetição** em branco, a macro será executada pelo número de vezes especificado.</span><span class="sxs-lookup"><span data-stu-id="f2959-133">If you enter a number for **Repeat Count** but leave **Repeat Expression** blank, the macro runs the specified number of times.</span></span>
> - <span data-ttu-id="f2959-134">Se você deixar **Contagem de repetição** em branco, mas inserir uma expressão em **Expressão de repetição**, a macro será executada até que a expressão avalie como **False**.</span><span class="sxs-lookup"><span data-stu-id="f2959-134">If you leave **Repeat Count** blank but enter an expression for **Repeat Expression**, the macro runs until the expression evaluates to **False**.</span></span>
> - <span data-ttu-id="f2959-135">Se você inserir valores para os dois argumentos, a macro será executada pelo número de vezes especificado em **Contagem de repetição** ou até que **Expressão de repetição** avalie como **False**, o que ocorrer primeiro.</span><span class="sxs-lookup"><span data-stu-id="f2959-135">If you enter values for both arguments, the macro runs the number of times specified in **Repeat Count** or until **Repeat Expression** evaluates to **False**, whichever occurs first.</span></span>

<span data-ttu-id="f2959-p106">Se uma macro contendo a ação **ExecutarMacro** for executada e ela alcançar a ação **ExecutarMacro**, o Access executará a macro chamada. Após a conclusão da macro chamada, o Access retornará à macro original e executará a próxima ação.</span><span class="sxs-lookup"><span data-stu-id="f2959-p106">When you run a macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called macro. When the called macro has finished, Access returns to the original macro and runs the next action.</span></span>

> [!NOTE]
> - <span data-ttu-id="f2959-138">É possível chamar uma macro do mesmo grupo de macros ou de outro grupo.</span><span class="sxs-lookup"><span data-stu-id="f2959-138">You can call a macro in the same macro group or in another macro group.</span></span>
> - <span data-ttu-id="f2959-p107">Você pode aninhar macros. Ou seja, você pode executar a macro A que, por sua vez, chama a macro B etc. Em cada caso, quando a macro chamada é concluída, o Access retorna à macro que a chamou e executa a próxima ação dessa macro.</span><span class="sxs-lookup"><span data-stu-id="f2959-p107">You can nest macros. That is, you can run macro A, which in turn calls macro B, and so on. In each case, when the called macro has finished, Access returns to the macro that called it and runs the next action in that macro.</span></span>

<span data-ttu-id="f2959-142">Para executar a ação **ExecutarMacro** em um módulo do VBA(Visual Basic for Applications), use o método **RunMacro** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="f2959-142">To run the **RunMacro** action in a Visual Basic for Applications (VBA) module, use the **RunMacro** method of the **DoCmd** object.</span></span>

