---
title: Acessar o código de XLL no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- acesso ao código de xll [excel 2007],XLLs [Excel 2007], acesso ao código,comandos [Excel 2007], registro,funções [Excel 2007], registro,chamar XLLs a partir do Excel,registrar comandos [Excel 2007],registrar funções [Excel 2007]
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d1332b0dffc052404c75c4ec51d94879457c3da0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304183"
---
# <a name="accessing-xll-code-in-excel"></a><span data-ttu-id="458b5-104">Acessar o código de XLL no Excel</span><span class="sxs-lookup"><span data-stu-id="458b5-104">Accessing XLL code in Excel</span></span>

<span data-ttu-id="458b5-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="458b5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="458b5-106">Para ficar acessível no Microsoft Excel, as funções e os comandos que um XLL contém:</span><span class="sxs-lookup"><span data-stu-id="458b5-106">To be accessible in Microsoft Excel, the functions and commands that an XLL contains:</span></span>
  
- <span data-ttu-id="458b5-107">Devem ser exportados pelo XLL.</span><span class="sxs-lookup"><span data-stu-id="458b5-107">Must be exported by the XLL.</span></span>
    
- <span data-ttu-id="458b5-108">Devem estar registrados no Excel.</span><span class="sxs-lookup"><span data-stu-id="458b5-108">Must be registered with Excel.</span></span>
    
## <a name="registering-functions-and-commands-with-excel"></a><span data-ttu-id="458b5-109">Como registrar comandos e funções no Excel</span><span class="sxs-lookup"><span data-stu-id="458b5-109">Registering functions and commands with Excel</span></span>

<span data-ttu-id="458b5-110">O registro informa o seguinte ao Excel sobre um ponto de entrada DLL:</span><span class="sxs-lookup"><span data-stu-id="458b5-110">Registration tells Excel the following about a DLL entry point:</span></span>
  
- <span data-ttu-id="458b5-111">Se está oculto ou, no caso de uma função, se está visível no Assistente de Função.</span><span class="sxs-lookup"><span data-stu-id="458b5-111">Whether it is hidden or, if a function, whether it is visible in the Function Wizard.</span></span>
    
- <span data-ttu-id="458b5-112">Se pode ser chamado somente de uma folha de macro XLM ou também de uma planilha.</span><span class="sxs-lookup"><span data-stu-id="458b5-112">Whether it is callable only from an XLM macro sheet, or also from a worksheet.</span></span>
    
- <span data-ttu-id="458b5-113">Quando é um comando, se é uma função de planilha ou uma função equivalente da folha de macro.</span><span class="sxs-lookup"><span data-stu-id="458b5-113">If a command, whether it is a worksheet function or a macro sheet equivalent function.</span></span>
    
- <span data-ttu-id="458b5-114">O que é o nome de exportação de XLL/DLL e qual nome deseja que o Excel use.</span><span class="sxs-lookup"><span data-stu-id="458b5-114">What its XLL/DLL export name is, and what name you want Excel to use.</span></span>
    
- <span data-ttu-id="458b5-115">Quando é uma função:</span><span class="sxs-lookup"><span data-stu-id="458b5-115">If it is a function:</span></span>
    
  - <span data-ttu-id="458b5-116">Quais tipos de dados ela retorna e recebe como argumentos.</span><span class="sxs-lookup"><span data-stu-id="458b5-116">What data types it returns and takes as arguments.</span></span>
    
  - <span data-ttu-id="458b5-117">Se retorna o resultado modificando um argumento em vigor.</span><span class="sxs-lookup"><span data-stu-id="458b5-117">Whether it returns its result by modifying an argument in place.</span></span>
    
  - <span data-ttu-id="458b5-118">Se é volátil.</span><span class="sxs-lookup"><span data-stu-id="458b5-118">Whether it is volatile.</span></span>
    
  - <span data-ttu-id="458b5-119">Se é isento de threads (com suporte a partir do Excel 2007).</span><span class="sxs-lookup"><span data-stu-id="458b5-119">Whether it is thread safe (supported starting in Excel 2007).</span></span>
    
  - <span data-ttu-id="458b5-120">Que texto o Assistente de função Colar e o editor de AutoCompletar devem exibir para ajudar a chamar a função.</span><span class="sxs-lookup"><span data-stu-id="458b5-120">What text the Paste Function Wizard and AutoComplete editor should display to help with calling the function.</span></span>
    
  - <span data-ttu-id="458b5-121">Qual categoria de função deveria ser listada.</span><span class="sxs-lookup"><span data-stu-id="458b5-121">Which function category it should be listed under.</span></span>
    
<span data-ttu-id="458b5-122">Tudo isso é obtido usando a função da API C [xlfRegister](xlfregister-form-1.md), equivalente à função XLM **REGISTER**.</span><span class="sxs-lookup"><span data-stu-id="458b5-122">This is all achieved using the C API function [xlfRegister](xlfregister-form-1.md), equivalent to the XLM function **REGISTER**.</span></span>
  
## <a name="calling-xll-functions-directly-from-excel"></a><span data-ttu-id="458b5-123">Como chamar funções de DLL diretamente do Excel</span><span class="sxs-lookup"><span data-stu-id="458b5-123">Calling XLL functions directly from Excel</span></span>

<span data-ttu-id="458b5-124">Após serem registradas, as funções de planilha e planilha de macro XLL podem ser chamadas de qualquer lugar em que uma função interna possa ser chamada:</span><span class="sxs-lookup"><span data-stu-id="458b5-124">Once they are registered, XLL worksheet and macro sheet functions can be called from anywhere a built-in function can be called from:</span></span>
  
- <span data-ttu-id="458b5-125">Uma fórmula de célula única ou matriz em uma planilha.</span><span class="sxs-lookup"><span data-stu-id="458b5-125">A single-cell or array formula on a worksheet.</span></span>
    
- <span data-ttu-id="458b5-126">Uma fórmula de célula única ou matriz em uma planilha de macro.</span><span class="sxs-lookup"><span data-stu-id="458b5-126">A single-cell or array formula on a macro sheet.</span></span>
    
- <span data-ttu-id="458b5-127">A definição de um nome definido.</span><span class="sxs-lookup"><span data-stu-id="458b5-127">The definition of a defined name.</span></span>
    
- <span data-ttu-id="458b5-128">Os campos de condição e limite em uma caixa de diálogo de formato condicional.</span><span class="sxs-lookup"><span data-stu-id="458b5-128">The condition and limit fields in a conditional format dialog box.</span></span>
    
- <span data-ttu-id="458b5-129">De outro suplemento por meio da função da API C [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="458b5-129">From another add-in via the C API function [xlUDF](xludf.md).</span></span>
    
- <span data-ttu-id="458b5-130">Do Visual Basic for Applications (VBA) por meio do método **Application.Run**.</span><span class="sxs-lookup"><span data-stu-id="458b5-130">From Visual Basic for Applications (VBA) via the **Application.Run** method.</span></span> 
    
<span data-ttu-id="458b5-131">Você pode obter uma referência à célula de chamada ou ao intervalo de células dentro de sua função usando a função da API C **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="458b5-131">You can obtain a reference to the calling cell or range of cells within your function using the C API function **xlfCaller**.</span></span> <span data-ttu-id="458b5-132">Se a função foi chamada da expressão de formato condicional da célula, ainda será retornada uma referência à célula ou células associadas, portanto, não é possível presumir que a fórmula da célula contenha a função de XLL.</span><span class="sxs-lookup"><span data-stu-id="458b5-132">If the function was called from the cell's conditional format expression, you are still returned a reference to the associated cell or cells, so you cannot assume that the cell's formula contains the XLL function.</span></span> <span data-ttu-id="458b5-133">Se sua função foi chamada de uma função definida pelo usuário do VBA (UDF), **xlfCaller** retorna novamente o endereço das células que chamaram a função VBA.</span><span class="sxs-lookup"><span data-stu-id="458b5-133">If your function was called from a VBA user-defined function (UDF), **xlfCaller** again returns the address of the cells that called the VBA function.</span></span> <span data-ttu-id="458b5-134">Para saber mais, confira [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="458b5-134">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="458b5-135">O Excel também chama funções de XLL no **Assistente de Função Colar** e caixas de diálogo **Substituir**.</span><span class="sxs-lookup"><span data-stu-id="458b5-135">Excel also calls XLL function code from the **Paste Function Wizard** and **Replace** dialog boxes.</span></span> <span data-ttu-id="458b5-136">Pode ser necessário restringir a execução normal de seu código no caso da caixa de diálogo **Argumentos da Função Colar**, especialmente onde sua função pode levar muito tempo para ser executada.</span><span class="sxs-lookup"><span data-stu-id="458b5-136">You might need to restrict your code's normal running in the case of the **Paste Function Arguments** dialog box, especially where your function can take a long time to execute.</span></span> <span data-ttu-id="458b5-137">Para detectar se sua função está sendo chamada de qualquer uma dessas caixas de diálogo, implemente código em seu projeto para percorrer todas as janelas abertas para determinar se a janela frontal é uma dessas caixas de diálogo e, em caso afirmativo, qual delas.</span><span class="sxs-lookup"><span data-stu-id="458b5-137">To detect if your function is being called from either of these dialog boxes, you must implement some code in your project that iterates through all the open windows to determine if the front window is one of these dialog boxes, and, if so, which one.</span></span> 
  
## <a name="calling-xll-commands-directly-from-excel"></a><span data-ttu-id="458b5-138">Como chamar comandos de XLL diretamente do Excel</span><span class="sxs-lookup"><span data-stu-id="458b5-138">Calling XLL commands directly from Excel</span></span>

<span data-ttu-id="458b5-139">Uma vez registrados, os comandos de XLL podem ser chamados de todas as maneiras que outras macros definidas pelo usuário podem ser chamadas:</span><span class="sxs-lookup"><span data-stu-id="458b5-139">Once they are registered, XLL commands can be called in all the ways that other user-defined macros can be called:</span></span>
  
- <span data-ttu-id="458b5-140">Por estarem associados a um objeto de controle incorporado a uma planilha.</span><span class="sxs-lookup"><span data-stu-id="458b5-140">By being associated with a control object embedded on a worksheet.</span></span>
    
- <span data-ttu-id="458b5-141">Na caixa de diálogo Executar Macro.</span><span class="sxs-lookup"><span data-stu-id="458b5-141">From the Run Macro dialog box.</span></span>
    
- <span data-ttu-id="458b5-142">De uma macro definida pelo usuário do VBA usando o método **Application.Run**.</span><span class="sxs-lookup"><span data-stu-id="458b5-142">From a VBA user-defined macro using the **Application.Run** method.</span></span> 
    
- <span data-ttu-id="458b5-143">De uma barra de ferramentas ou item de menu personalizado.</span><span class="sxs-lookup"><span data-stu-id="458b5-143">From a customized menu item or toolbar.</span></span>
    
- <span data-ttu-id="458b5-144">Usar um pressionamento de tecla de atalho configurado ao registrar o comando.</span><span class="sxs-lookup"><span data-stu-id="458b5-144">Using a shortcut keystroke set up when registering the command.</span></span>
    
- <span data-ttu-id="458b5-145">Como o comando a ser executado quando um evento especificado é interceptado.</span><span class="sxs-lookup"><span data-stu-id="458b5-145">As the command to be run when a specified event is trapped.</span></span>
    
> [!NOTE]
> <span data-ttu-id="458b5-146">Os comandos de XLL estão ocultos porque não aparecem na lista de macros disponíveis nas caixas de diálogo do Excel.</span><span class="sxs-lookup"><span data-stu-id="458b5-146">XLL commands are hidden in that they do not appear on the list of available macros in Excel dialog boxes.</span></span> <span data-ttu-id="458b5-147">No entanto, podem ser inseridos manualmente no campo de nome da macro.</span><span class="sxs-lookup"><span data-stu-id="458b5-147">But they can be entered manually into the macro name field.</span></span> <span data-ttu-id="458b5-148">O Excel espera o nome registrado como está nessas caixas de diálogo, não o nome de exportação de DLL.</span><span class="sxs-lookup"><span data-stu-id="458b5-148">Excel expects the registered-as name in these dialog boxes, not the DLL export name.</span></span> 
  
<span data-ttu-id="458b5-149">Todos os comandos de XLL registrados com o Excel são considerados pelo Excel da forma a seguir:</span><span class="sxs-lookup"><span data-stu-id="458b5-149">All XLL commands registered with Excel are assumed by Excel to be of the following form:</span></span>
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

<span data-ttu-id="458b5-p104">O Excel ignora o valor de retorno, a menos que ele seja chamado de uma planilha de macro XLM; neste caso, o valor de retorno é convertido para **TRUE** ou **FALSE**. Portanto, você deve retornar 1 se o comando foi executado com sucesso e 0 se falhou ou foi cancelado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="458b5-p104">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span>
  
<span data-ttu-id="458b5-152">Você pode obter informações sobre a forma como o comando foi invocado usando a função da API C **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="458b5-152">You can obtain information about how your command was invoked using the C API function **xlfCaller**.</span></span> <span data-ttu-id="458b5-153">Para saber mais, confira [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="458b5-153">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
<span data-ttu-id="458b5-154">Iniciar na interface do usuário do Excel 2007 é muito diferente das versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="458b5-154">Starting in Excel 2007 user interface is very different from earlier versions.</span></span> <span data-ttu-id="458b5-155">As funções da API C que permitem a adição e exclusão de barras de menus personalizadas, menus, submenus, itens de menu, barras de ferramentas personalizadas e botões da barra de ferramentas ainda têm suporte na maioria dos casos.</span><span class="sxs-lookup"><span data-stu-id="458b5-155">The C API functions that permit the addition and deletion of custom menu bars, menus, submenus, menu items, custom toolbars and toolbar buttons are still supported in most cases.</span></span> <span data-ttu-id="458b5-156">No entanto, elas nem sempre disponibilizam o item adicionado na forma que os usuários já conhecem.</span><span class="sxs-lookup"><span data-stu-id="458b5-156">However, they may not always make the added item available in a way that your users are familiar with.</span></span> <span data-ttu-id="458b5-157">Você deve verificar cuidadosamente se alguma funcionalidade adicional ainda está acessível ou implementar uma personalização específica da versão.</span><span class="sxs-lookup"><span data-stu-id="458b5-157">You should carefully check that any added functionality is still accessible, or implement a version-specific customization.</span></span> <span data-ttu-id="458b5-158">A partir do Excel 2007, a interface do usuário é personalizada de forma mais eficaz usando um módulo de código gerenciado que pode ser fortemente acoplado aos comandos de XLL.</span><span class="sxs-lookup"><span data-stu-id="458b5-158">Starting in Excel 2007 the user interface is best customized by using a managed code module that can then be tightly coupled to your XLL commands.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="458b5-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="458b5-159">See also</span></span>

- [<span data-ttu-id="458b5-160">Como criar XLLs</span><span class="sxs-lookup"><span data-stu-id="458b5-160">Creating XLLs</span></span>](creating-xlls.md)
- [<span data-ttu-id="458b5-161">Chamar funções de XLL no Assistente de Função ou nas caixas de diálogo Substituir</span><span class="sxs-lookup"><span data-stu-id="458b5-161">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [<span data-ttu-id="458b5-162">Gerenciador de Suplemento e Funções da Interface XLL</span><span class="sxs-lookup"><span data-stu-id="458b5-162">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
- [<span data-ttu-id="458b5-163">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="458b5-163">Developing Excel XLLs</span></span>](developing-excel-xlls.md)



