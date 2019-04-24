---
title: Permitir quebras de usuário em operações deMoradas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- função xlAbort [Excel 2007], tarefas simultâneas [Excel 2007], o usuário quebra [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310378"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="a16b9-104">Permitir quebras de usuário em operações deMoradas</span><span class="sxs-lookup"><span data-stu-id="a16b9-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="a16b9-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a16b9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a16b9-106">Embora o Windows Use multitarefas preemptivas, onde suas funções ou comandos podem levar muito tempo para serem executados, é uma boa prática levar algum tempo para o sistema operacional agora e novamente para ajudá-lo a agendar tarefas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a16b9-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="a16b9-107">Usando chamadas nativas do Windows, você pode fazer isso usando a função Sleep.</span><span class="sxs-lookup"><span data-stu-id="a16b9-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="a16b9-108">Usando a API C, você pode fazer isso usando a [função xlAbort](xlabort.md), que não só produz o processador para um instante, mas também verifica se o usuário pressionou a tecla Cancelar, **ESC**.</span><span class="sxs-lookup"><span data-stu-id="a16b9-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="a16b9-109">Portanto, a função **xlAbort** permite que o código Verifique se o usuário deseja finalizar o processo, faça a limpeza necessária e, em seguida, retorne o controle para o Excel.</span><span class="sxs-lookup"><span data-stu-id="a16b9-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="a16b9-110">A função também permite que você desmarque a condição de interrupção.</span><span class="sxs-lookup"><span data-stu-id="a16b9-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="a16b9-111">Isso permite que os comandos exibam uma caixa de diálogo para verificar se o usuário deseja encerrar o comando.</span><span class="sxs-lookup"><span data-stu-id="a16b9-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="a16b9-112">Se o usuário não quiser encerrar o comando, chamar a função **xlAbort** com o argumento *false* desmarcará a quebra.</span><span class="sxs-lookup"><span data-stu-id="a16b9-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="a16b9-113">(O argumento padrão é *true* , que simplesmente verifica a condição, mas não a limpa.)</span><span class="sxs-lookup"><span data-stu-id="a16b9-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="a16b9-114">Você pode chamar a função **xlAbort** de uma função definida pelo usuário (UDF) ou de um comando XLL.</span><span class="sxs-lookup"><span data-stu-id="a16b9-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="a16b9-115">Em um UDF, quando a função **xlAbort** retorna **true**, tendo detectado uma quebra de usuário, você normalmente recortou curto o cálculo da função e retorna um valor para indicar que o cálculo não foi concluído, talvez um erro ou zero.</span><span class="sxs-lookup"><span data-stu-id="a16b9-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="a16b9-116">Você não desmarcaria a condição de interrupção para que outras instâncias de funções demoradas também marquem esta condição também sejam interrompidas.</span><span class="sxs-lookup"><span data-stu-id="a16b9-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="a16b9-117">O Excel desmarca implicitamente essa condição quando um recálculo termina.</span><span class="sxs-lookup"><span data-stu-id="a16b9-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="a16b9-118">Quando você detecta uma condição de interrupção em um comando, normalmente limpa a condição chamando a função **xlAbort** novamente com o argumento **false**, embora o Excel desmarque implicitamente essa condição quando um comando termina.</span><span class="sxs-lookup"><span data-stu-id="a16b9-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a16b9-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a16b9-119">See also</span></span>



[<span data-ttu-id="a16b9-120">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="a16b9-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="a16b9-121">Recálculo com vários threads no Excel</span><span class="sxs-lookup"><span data-stu-id="a16b9-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="a16b9-122">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="a16b9-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="a16b9-123">Acessar a instância do Excel e as alças da janela principal</span><span class="sxs-lookup"><span data-stu-id="a16b9-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

