---
title: Acessando código XLL no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- acessando código xll [excel 2007], XLLs [Excel 2007], acessando código, comandos [Excel 2007], registro, funções [Excel 2007], registro, chamando XLLs do Excel, registrando comandos [Excel 2007], registrando funções [Excel 2007]
localization_priority: Normal
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1523f9e8213cb955f1bfd995c42f921b001299fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765260"
---
# <a name="accessing-xll-code-in-excel"></a><span data-ttu-id="f7729-104">Acessando código XLL no Excel</span><span class="sxs-lookup"><span data-stu-id="f7729-104">Accessing XLL code in Excel</span></span>

<span data-ttu-id="f7729-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7729-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f7729-106">Seja acessível no Microsoft Excel, as funções e comandos que contém um XLL:</span><span class="sxs-lookup"><span data-stu-id="f7729-106">To be accessible in Microsoft Excel, the functions and commands that an XLL contains:</span></span>
  
- <span data-ttu-id="f7729-107">Deve ser exportados pelo XLL.</span><span class="sxs-lookup"><span data-stu-id="f7729-107">Must be exported by the XLL.</span></span>
    
- <span data-ttu-id="f7729-108">Deve ser registrado com o Excel.</span><span class="sxs-lookup"><span data-stu-id="f7729-108">Must be registered with Excel.</span></span>
    
## <a name="registering-functions-and-commands-with-excel"></a><span data-ttu-id="f7729-109">Registrando as funções e comandos com o Excel</span><span class="sxs-lookup"><span data-stu-id="f7729-109">Registering functions and commands with Excel</span></span>

<span data-ttu-id="f7729-110">Registro informa Excel a seguir sobre um ponto de entrada DLL:</span><span class="sxs-lookup"><span data-stu-id="f7729-110">Registration tells Excel the following about a DLL entry point:</span></span>
  
- <span data-ttu-id="f7729-111">Se ele estiver oculto ou se uma função, se ele estiver visível no Assistente de função.</span><span class="sxs-lookup"><span data-stu-id="f7729-111">Whether it is hidden or, if a function, whether it is visible in the Function Wizard.</span></span>
    
- <span data-ttu-id="f7729-112">Se ele está acessível somente a partir de uma folha de macro XLM ou também uma planilha.</span><span class="sxs-lookup"><span data-stu-id="f7729-112">Whether it is callable only from an XLM macro sheet, or also from a worksheet.</span></span>
    
- <span data-ttu-id="f7729-113">Se um comando, se é uma função de planilha ou uma função equivalente de folha de macro.</span><span class="sxs-lookup"><span data-stu-id="f7729-113">If a command, whether it is a worksheet function or a macro sheet equivalent function.</span></span>
    
- <span data-ttu-id="f7729-114">Qual é o seu nome de exportação XLL/DLL e que nome que você deseja que o Excel use.</span><span class="sxs-lookup"><span data-stu-id="f7729-114">What its XLL/DLL export name is, and what name you want Excel to use.</span></span>
    
- <span data-ttu-id="f7729-115">Se ele é uma função:</span><span class="sxs-lookup"><span data-stu-id="f7729-115">If it is a function:</span></span>
    
  - <span data-ttu-id="f7729-116">Quais dados retorna as digita e utiliza como argumentos.</span><span class="sxs-lookup"><span data-stu-id="f7729-116">What data types it returns and takes as arguments.</span></span>
    
  - <span data-ttu-id="f7729-117">Se ela retorna seu resultado modificando um argumento in-loco.</span><span class="sxs-lookup"><span data-stu-id="f7729-117">Whether it returns its result by modifying an argument in place.</span></span>
    
  - <span data-ttu-id="f7729-118">Se ele está voláteis.</span><span class="sxs-lookup"><span data-stu-id="f7729-118">Whether it is volatile.</span></span>
    
  - <span data-ttu-id="f7729-119">Se ele está thread-safe (começando com suporte no Excel 2007).</span><span class="sxs-lookup"><span data-stu-id="f7729-119">Whether it is thread safe (supported starting in Excel 2007).</span></span>
    
  - <span data-ttu-id="f7729-120">O que o Assistente de função colar de texto e o editor de AutoCompletar devem ser exibida para ajudá-lo com chamar a função.</span><span class="sxs-lookup"><span data-stu-id="f7729-120">What text the Paste Function Wizard and AutoComplete editor should display to help with calling the function.</span></span>
    
  - <span data-ttu-id="f7729-121">Qual funcionar categoria, em que ele deve estar listado.</span><span class="sxs-lookup"><span data-stu-id="f7729-121">Which function category it should be listed under.</span></span>
    
<span data-ttu-id="f7729-122">Tudo isso é obtido usando a API C função [xlfRegister](xlfregister-form-1.md), equivalente à função XLM **registrar**.</span><span class="sxs-lookup"><span data-stu-id="f7729-122">This is all achieved using the C API function [xlfRegister](xlfregister-form-1.md), equivalent to the XLM function **REGISTER**.</span></span>
  
## <a name="calling-xll-functions-directly-from-excel"></a><span data-ttu-id="f7729-123">Chamando funções XLL diretamente do Excel</span><span class="sxs-lookup"><span data-stu-id="f7729-123">Calling XLL functions directly from Excel</span></span>

<span data-ttu-id="f7729-124">Depois que eles são registrados, as funções de folha de macro e de planilha XLL podem ser chamadas em qualquer lugar, de que uma função incorporada pode ser chamada:</span><span class="sxs-lookup"><span data-stu-id="f7729-124">Once they are registered, XLL worksheet and macro sheet functions can be called from anywhere a built-in function can be called from:</span></span>
  
- <span data-ttu-id="f7729-125">Uma fórmula de célula única ou matriz em uma planilha.</span><span class="sxs-lookup"><span data-stu-id="f7729-125">A single-cell or array formula on a worksheet.</span></span>
    
- <span data-ttu-id="f7729-126">Uma fórmula de célula única ou matriz em uma folha de macro.</span><span class="sxs-lookup"><span data-stu-id="f7729-126">A single-cell or array formula on a macro sheet.</span></span>
    
- <span data-ttu-id="f7729-127">A definição de um nome definido.</span><span class="sxs-lookup"><span data-stu-id="f7729-127">The definition of a defined name.</span></span>
    
- <span data-ttu-id="f7729-128">Os campos de condição e limite em uma caixa de diálogo formato condicional.</span><span class="sxs-lookup"><span data-stu-id="f7729-128">The condition and limit fields in a conditional format dialog box.</span></span>
    
- <span data-ttu-id="f7729-129">De outro suplemento por meio da API C funcione [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="f7729-129">From another add-in via the C API function [xlUDF](xludf.md).</span></span>
    
- <span data-ttu-id="f7729-130">No Visual Basic for Applications (VBA) por meio do método **Run** .</span><span class="sxs-lookup"><span data-stu-id="f7729-130">From Visual Basic for Applications (VBA) via the **Application.Run** method.</span></span> 
    
<span data-ttu-id="f7729-131">Você pode obter uma referência para a célula ou intervalo de células de chamada dentro de sua função usando a função do C API **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="f7729-131">You can obtain a reference to the calling cell or range of cells within your function using the C API function **xlfCaller**.</span></span> <span data-ttu-id="f7729-132">Se a função foi chamada de expressão de formatação condicional da célula, você ainda retorna uma referência para a célula associada ou células, portanto você não pode assumir que a fórmula da célula contém a função XLL.</span><span class="sxs-lookup"><span data-stu-id="f7729-132">If the function was called from the cell's conditional format expression, you are still returned a reference to the associated cell or cells, so you cannot assume that the cell's formula contains the XLL function.</span></span> <span data-ttu-id="f7729-133">Se a sua função foi chamada a partir de uma função definida pelo usuário do VBA (UDF), o **xlfCaller** novamente devolve o endereço das células que a chamada de função do VBA.</span><span class="sxs-lookup"><span data-stu-id="f7729-133">If your function was called from a VBA user-defined function (UDF), **xlfCaller** again returns the address of the cells that called the VBA function.</span></span> <span data-ttu-id="f7729-134">Para obter mais informações, consulte [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="f7729-134">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="f7729-135">Excel também chama o código de função XLL de caixas de diálogo **Assistente de função colar** e **Substituir** .</span><span class="sxs-lookup"><span data-stu-id="f7729-135">Excel also calls XLL function code from the **Paste Function Wizard** and **Replace** dialog boxes.</span></span> <span data-ttu-id="f7729-136">Talvez seja necessário restringir seu código normal em execução no caso da caixa de diálogo **Argumentos da função colar** , especialmente onde sua função pode levar muito tempo para executar.</span><span class="sxs-lookup"><span data-stu-id="f7729-136">You might need to restrict your code's normal running in the case of the **Paste Function Arguments** dialog box, especially where your function can take a long time to execute.</span></span> <span data-ttu-id="f7729-137">Para detectar se a sua função está sendo chamada de qualquer um dessas caixas de diálogo, você deve implementar alguns códigos em seu projeto que itera todas as janelas abertas para determinar se a janela front é uma dessas caixas de diálogo e, em caso afirmativo, qual deles.</span><span class="sxs-lookup"><span data-stu-id="f7729-137">To detect if your function is being called from either of these dialog boxes, you must implement some code in your project that iterates through all the open windows to determine if the front window is one of these dialog boxes, and, if so, which one.</span></span> 
  
## <a name="calling-xll-commands-directly-from-excel"></a><span data-ttu-id="f7729-138">Chamar comandos XLL diretamente do Excel</span><span class="sxs-lookup"><span data-stu-id="f7729-138">Calling XLL commands directly from Excel</span></span>

<span data-ttu-id="f7729-139">Depois que eles são registrados, comandos XLL podem ser chamados em todas as formas que outras macros definidas pelo usuário podem ser chamadas:</span><span class="sxs-lookup"><span data-stu-id="f7729-139">Once they are registered, XLL commands can be called in all the ways that other user-defined macros can be called:</span></span>
  
- <span data-ttu-id="f7729-140">Por sendo associado a um objeto control incorporadas em uma planilha.</span><span class="sxs-lookup"><span data-stu-id="f7729-140">By being associated with a control object embedded on a worksheet.</span></span>
    
- <span data-ttu-id="f7729-141">Na caixa de diálogo Executar Macro.</span><span class="sxs-lookup"><span data-stu-id="f7729-141">From the Run Macro dialog box.</span></span>
    
- <span data-ttu-id="f7729-142">De uma macro VBA definidas pelo usuário, usando o método Application **Run** .</span><span class="sxs-lookup"><span data-stu-id="f7729-142">From a VBA user-defined macro using the **Application.Run** method.</span></span> 
    
- <span data-ttu-id="f7729-143">A partir de um item de menu personalizado ou uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="f7729-143">From a customized menu item or toolbar.</span></span>
    
- <span data-ttu-id="f7729-144">Usando um pressionamento de tecla de atalho configurar ao registrar o comando.</span><span class="sxs-lookup"><span data-stu-id="f7729-144">Using a shortcut keystroke set up when registering the command.</span></span>
    
- <span data-ttu-id="f7729-145">Como o comando a ser executado quando um evento específico é interceptado.</span><span class="sxs-lookup"><span data-stu-id="f7729-145">As the command to be run when a specified event is trapped.</span></span>
    
> [!NOTE]
> <span data-ttu-id="f7729-146">Comandos XLL estão ocultos em que eles não apareçam na lista de macros disponíveis nas caixas de diálogo do Excel.</span><span class="sxs-lookup"><span data-stu-id="f7729-146">XLL commands are hidden in that they do not appear on the list of available macros in Excel dialog boxes.</span></span> <span data-ttu-id="f7729-147">Mas podem ser inseridos manualmente no campo nome da macro.</span><span class="sxs-lookup"><span data-stu-id="f7729-147">But they can be entered manually into the macro name field.</span></span> <span data-ttu-id="f7729-148">Excel espera que o nome registrado como essas caixas de diálogo, não o nome da DLL export.</span><span class="sxs-lookup"><span data-stu-id="f7729-148">Excel expects the registered-as name in these dialog boxes, not the DLL export name.</span></span> 
  
<span data-ttu-id="f7729-149">Todos os comandos XLL registrados com o Excel diferenciam pelo Excel deve estar no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="f7729-149">All XLL commands registered with Excel are assumed by Excel to be of the following form:</span></span>
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

<span data-ttu-id="f7729-p104">[!OBSERVA��O] O Excel ignorar� o valor de retorno, a menos que ele seja chamado de uma folha de macros XLM; nesse caso, o valor de retorno ser� convertido em **TRUE** ou em **FALSE**. Dessa forma, voc� dever� retornar 1 se o seu comando tiver sido executado com �xito e 0 caso ele tenha falhado ou tenha sido cancelado pelo usu�rio.</span><span class="sxs-lookup"><span data-stu-id="f7729-p104">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span>
  
<span data-ttu-id="f7729-152">Você pode obter informações sobre como seu comando foi invocado usando a API C funcionar **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="f7729-152">You can obtain information about how your command was invoked using the C API function **xlfCaller**.</span></span> <span data-ttu-id="f7729-153">Para obter mais informações, consulte [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="f7729-153">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
<span data-ttu-id="f7729-154">Iniciar na interface de usuário do Excel 2007 é muito diferente das versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="f7729-154">Starting in Excel 2007 user interface is very different from earlier versions.</span></span> <span data-ttu-id="f7729-155">As funções da API C que permitem a adição e a exclusão de barras de menus personalizados, menus, submenus, itens de menu, barras de ferramentas personalizadas e botões de barra de ferramentas que ainda são suportadas na maioria dos casos.</span><span class="sxs-lookup"><span data-stu-id="f7729-155">The C API functions that permit the addition and deletion of custom menu bars, menus, submenus, menu items, custom toolbars and toolbar buttons are still supported in most cases.</span></span> <span data-ttu-id="f7729-156">No entanto, eles podem não sempre disponibilize o item adicionado de forma que os usuários estão familiarizados com.</span><span class="sxs-lookup"><span data-stu-id="f7729-156">However, they may not always make the added item available in a way that your users are familiar with.</span></span> <span data-ttu-id="f7729-157">Você deve verificar cuidadosamente se qualquer funcionalidade adicionada ainda pode ser acessado ou implementar uma personalização específicos da versão.</span><span class="sxs-lookup"><span data-stu-id="f7729-157">You should carefully check that any added functionality is still accessible, or implement a version-specific customization.</span></span> <span data-ttu-id="f7729-158">Iniciando no Excel 2007 a interface do usuário é melhor personalizado usando um módulo de código gerenciado que pode então ser fortemente agrupado a seus comandos XLL.</span><span class="sxs-lookup"><span data-stu-id="f7729-158">Starting in Excel 2007 the user interface is best customized by using a managed code module that can then be tightly coupled to your XLL commands.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f7729-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7729-159">See also</span></span>

- [<span data-ttu-id="f7729-160">Criando XLLs</span><span class="sxs-lookup"><span data-stu-id="f7729-160">Creating XLLs</span></span>](creating-xlls.md)
- [<span data-ttu-id="f7729-161">Funções do Assistente de função ou caixas de diálogo Replace XLL chamada</span><span class="sxs-lookup"><span data-stu-id="f7729-161">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [<span data-ttu-id="f7729-162">Gerenciador de suplemento e funções da Interface XLL</span><span class="sxs-lookup"><span data-stu-id="f7729-162">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
- [<span data-ttu-id="f7729-163">Developing Excel XLLs</span><span class="sxs-lookup"><span data-stu-id="f7729-163">Developing Excel XLLs</span></span>](developing-excel-xlls.md)



