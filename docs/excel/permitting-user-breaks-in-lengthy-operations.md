---
title: Quebras de autorizações de usuário em operações demoradas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- função xlAbort [excel 2007], tarefas simultâneas [Excel 2007], quebras de usuário [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b13f9b9a8c0e5621b25df13537632bdbe5dfc29e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765427"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="8b6bf-104">Quebras de autorizações de usuário em operações demoradas</span><span class="sxs-lookup"><span data-stu-id="8b6bf-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="8b6bf-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8b6bf-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8b6bf-106">Embora o Windows usa preventivo multitarefa, onde suas funções ou comandos podem levar muito tempo para executar, é uma boa prática para gerar algum tempo para o sistema operacional agora e novamente para ajudá-lo a agendar tarefas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="8b6bf-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="8b6bf-107">Usando as chamadas nativas do Windows, você pode fazer isso usando a função de suspensão.</span><span class="sxs-lookup"><span data-stu-id="8b6bf-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="8b6bf-108">Usando a API C, você pode executá-la usando a [função xlAbort](xlabort.md), que não só produz o processador para uma instantânea, mas também verifica se o usuário pressiona a tecla de cancelar, **ESC**.</span><span class="sxs-lookup"><span data-stu-id="8b6bf-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="8b6bf-109">A função **xlAbort** , portanto, permite que o seu código para verificar se o usuário deseja finalizar o processo, faça a limpeza necessária e devolver o controle para o Excel.</span><span class="sxs-lookup"><span data-stu-id="8b6bf-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="8b6bf-110">A função também permite que você limpar a condição de quebra.</span><span class="sxs-lookup"><span data-stu-id="8b6bf-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="8b6bf-111">Isso permite que seus comandos exibir uma caixa de diálogo para verificar se o usuário deseja finalizar o comando.</span><span class="sxs-lookup"><span data-stu-id="8b6bf-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="8b6bf-112">Se não quiser que o usuário encerrar o comando, chamar a função **xlAbort** com o argumento *FALSE* limpa a quebra.</span><span class="sxs-lookup"><span data-stu-id="8b6bf-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="8b6bf-113">(O argumento padrão é *TRUE* , o que simplesmente verifica a condição, mas não desmarcou.)</span><span class="sxs-lookup"><span data-stu-id="8b6bf-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="8b6bf-114">Você pode chamar a função **xlAbort** a partir de uma função definida pelo usuário (UDF) ou um comando XLL.</span><span class="sxs-lookup"><span data-stu-id="8b6bf-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="8b6bf-115">Em um UDF, quando a função **xlAbort** retorna **TRUE**, tendo detectada uma quebra de usuário, você faria normalmente cortar curto cálculo da função e retornar algum valor para indicar que o cálculo não foi concluída, talvez qualquer erro ou zero.</span><span class="sxs-lookup"><span data-stu-id="8b6bf-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="8b6bf-116">Desmarque a condição de quebra não para que outras instâncias de funções longas que também verificam essa condição também serão desfeitos.</span><span class="sxs-lookup"><span data-stu-id="8b6bf-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="8b6bf-117">Excel implicitamente limpa essa condição quando um recálculo for encerrada.</span><span class="sxs-lookup"><span data-stu-id="8b6bf-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="8b6bf-118">Quando você detectar uma condição de quebra em um comando, você geralmente desmarcar a condição chamando a função **xlAbort** novamente com o argumento **Falso**, embora Excel implicitamente limpa essa condição quando um comando for encerrada.</span><span class="sxs-lookup"><span data-stu-id="8b6bf-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8b6bf-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b6bf-119">See also</span></span>



[<span data-ttu-id="8b6bf-120">Funções da API C que podem ser chamadas apenas por um DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="8b6bf-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="8b6bf-121">Recálculo multithreaded no Excel</span><span class="sxs-lookup"><span data-stu-id="8b6bf-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="8b6bf-122">Developing Excel XLLs</span><span class="sxs-lookup"><span data-stu-id="8b6bf-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="8b6bf-123">Acessar a instância do Excel e as alças da janela principal</span><span class="sxs-lookup"><span data-stu-id="8b6bf-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

