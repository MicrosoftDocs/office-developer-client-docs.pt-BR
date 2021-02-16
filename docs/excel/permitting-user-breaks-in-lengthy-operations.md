---
title: Permitir quebras de usuário em operações demoradas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- função xlabort [excel 2007],tarefas simultâneas [Excel 2007],quebras de usuário [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414687"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="8df34-104">Permitir quebras de usuário em operações demoradas</span><span class="sxs-lookup"><span data-stu-id="8df34-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="8df34-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8df34-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8df34-106">Embora o Windows use multitarefa preventiva, onde suas funções ou comandos podem levar muito tempo para ser executado, é uma boa prática gerar algum tempo para o sistema operacional agora e novamente para ajudá-lo a agendar tarefas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="8df34-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="8df34-107">Usando chamadas nativas do Windows, você pode fazer isso usando a função de sleep.</span><span class="sxs-lookup"><span data-stu-id="8df34-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="8df34-108">Usando a API de C, você pode fazer isso usando a função [xlAbort](xlabort.md), que não só produz o processador por um instantâneo, mas também verifica se o usuário pressionou a tecla de cancelamento, **ESC**.</span><span class="sxs-lookup"><span data-stu-id="8df34-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="8df34-109">A **função xlAbort,** portanto, permite que seu código verifique se o usuário deseja finalizar o processo, fazer a limpeza necessária e retornar o controle para o Excel.</span><span class="sxs-lookup"><span data-stu-id="8df34-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="8df34-110">A função também permite limpar a condição de quebra.</span><span class="sxs-lookup"><span data-stu-id="8df34-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="8df34-111">Isso permite que seus comandos exibem uma caixa de diálogo para verificar se o usuário deseja finalizar o comando.</span><span class="sxs-lookup"><span data-stu-id="8df34-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="8df34-112">Se o usuário não quiser finalizar o comando, chamar a função **xlAbort** com o argumento  *FALSE*  limpará a pausa.</span><span class="sxs-lookup"><span data-stu-id="8df34-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="8df34-113">(O argumento padrão é  *TRUE*  , que simplesmente verifica a condição, mas não a limpa.)</span><span class="sxs-lookup"><span data-stu-id="8df34-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="8df34-114">Você pode chamar a **função xlAbort** a partir de uma função definida pelo usuário (UDF) ou de um comando XLL.</span><span class="sxs-lookup"><span data-stu-id="8df34-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="8df34-115">Em uma UDF, quando a função **xlAbort** retorna **VERDADEIRO**, após detectar uma quebra de usuário, você normalmente cortaria o cálculo da função e retornaria algum valor para indicar que o cálculo não foi concluído, talvez um erro ou zero.</span><span class="sxs-lookup"><span data-stu-id="8df34-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="8df34-116">Você não limparia a condição de quebra para que outras instâncias de funções longas que também verificam essa condição também quebram.</span><span class="sxs-lookup"><span data-stu-id="8df34-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="8df34-117">O Excel limpa implicitamente essa condição quando um recálculo termina.</span><span class="sxs-lookup"><span data-stu-id="8df34-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="8df34-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span><span class="sxs-lookup"><span data-stu-id="8df34-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8df34-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="8df34-119">See also</span></span>



[<span data-ttu-id="8df34-120">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="8df34-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="8df34-121">Recálculo com vários threads no Excel</span><span class="sxs-lookup"><span data-stu-id="8df34-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="8df34-122">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="8df34-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="8df34-123">Acessar a instância do Excel e as alças da janela principal</span><span class="sxs-lookup"><span data-stu-id="8df34-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

