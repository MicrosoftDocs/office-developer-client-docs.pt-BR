---
title: Multithreading e contenção de memória no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- multithreading em excel, contenção de memória no Excel, funções [Excel 2007], thread-safe, thread-safe funciona memória local de segmento de [Excel 2007], [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fb0eddfff2f34307143bb896fd451de357f2b639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765432"
---
# <a name="multithreading-and-memory-contention-in-excel"></a><span data-ttu-id="811d9-104">Multithreading e contenção de memória no Excel</span><span class="sxs-lookup"><span data-stu-id="811d9-104">Multithreading and Memory Contention in Excel</span></span>

 <span data-ttu-id="811d9-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="811d9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="811d9-106">Versões anteriores do Microsoft Excel que o Excel 2007 usam um único segmento para todos os cálculos da planilha.</span><span class="sxs-lookup"><span data-stu-id="811d9-106">Versions of Microsoft Excel earlier than Excel 2007 use a single thread for all worksheet calculations.</span></span> <span data-ttu-id="811d9-107">No entanto, a partir do Excel 2007, Excel pode ser configurado para usar de 1 segmentos simultâneos de 1024 para cálculo da planilha.</span><span class="sxs-lookup"><span data-stu-id="811d9-107">However, starting in Excel 2007, Excel can be configured to use from 1 to 1024 concurrent threads for worksheet calculation.</span></span> <span data-ttu-id="811d9-108">Em um computador com vários processadores ou vários núcleo, o número de threads padrão é igual ao número de processadores ou núcleos.</span><span class="sxs-lookup"><span data-stu-id="811d9-108">On a multi-processor or multi-core computer, the default number of threads is equal to the number of processors or cores.</span></span> <span data-ttu-id="811d9-109">Portanto, as células de thread-safe ou células que contêm apenas a funções que são thread-safe, podem ser reservadas para segmentos simultâneos, sujeito a lógica de recálculo usuais para serem calculadas após seus precedentes.</span><span class="sxs-lookup"><span data-stu-id="811d9-109">Therefore, thread-safe cells, or cells that only contain functions that are thread safe, can be allotted to concurrent threads, subject to the usual recalculation logic of needing to be calculated after their precedents.</span></span>
  
## <a name="thread-safe-functions"></a><span data-ttu-id="811d9-110">Funções thread-Safe</span><span class="sxs-lookup"><span data-stu-id="811d9-110">Thread-Safe Functions</span></span>

<span data-ttu-id="811d9-111">A maioria das funções de planilha internas iniciada no Excel 2007 são thread-safe.</span><span class="sxs-lookup"><span data-stu-id="811d9-111">Most of the built-in worksheet functions starting in Excel 2007 are thread safe.</span></span> <span data-ttu-id="811d9-112">Você também pode gravar e registrar as funções XLL como sendo thread-safe.</span><span class="sxs-lookup"><span data-stu-id="811d9-112">You can also write and register XLL functions as being thread safe.</span></span> <span data-ttu-id="811d9-113">O Excel usa um segmento (seu segmento principal) para chamar todos os comandos, funções thread-inseguras, funções **xlAuto** (exceto [xlAutoFree](xlautofree-xlautofree12.md) e **xlAutoFree12**) e COM e do Visual Basic para funções Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="811d9-113">Excel uses one thread (its main thread) to call all commands, thread-unsafe functions, **xlAuto** functions (except [xlAutoFree](xlautofree-xlautofree12.md) and **xlAutoFree12**), and COM and Visual Basic for Applications (VBA) functions.</span></span>
  
<span data-ttu-id="811d9-114">Onde uma função XLL retorna uma **XLOPER** ou **XLOPER12** com **xlbitDLLFree** definido, o Excel usa o mesmo thread em que a chamada de função foi feita para chamar **xlAutoFree** ou **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="811d9-114">Where an XLL function returns an **XLOPER** or **XLOPER12** with **xlbitDLLFree** set, Excel uses the same thread on which the function call was made to call **xlAutoFree** or **xlAutoFree12**.</span></span> <span data-ttu-id="811d9-115">A chamada para **xlAutoFree** ou **xlAutoFree12** é feita antes da próxima chamada de função naquele segmento.</span><span class="sxs-lookup"><span data-stu-id="811d9-115">The call to **xlAutoFree** or **xlAutoFree12** is made before the next function call on that thread.</span></span> 
  
<span data-ttu-id="811d9-116">Para os desenvolvedores XLL, existem benefícios para a criação de funções thread-safe:</span><span class="sxs-lookup"><span data-stu-id="811d9-116">For XLL developers, there are benefits for creating thread-safe functions:</span></span>
  
- <span data-ttu-id="811d9-117">Eles permitem que o Excel para fazer o máximo de um computador com vários processadores ou vários núcleo.</span><span class="sxs-lookup"><span data-stu-id="811d9-117">They allow Excel to make the most of a multi-processor or multi-core computer.</span></span>
    
- <span data-ttu-id="811d9-118">Eles abrem a possibilidade de usar servidores remotos muito mais eficiente do que pode ser realizado usando um único segmento.</span><span class="sxs-lookup"><span data-stu-id="811d9-118">They open up the possibility of using remote servers much more efficiently than can be done using a single thread.</span></span>
    
<span data-ttu-id="811d9-119">Suponha que você tem um computador com processador único que tenha sido configurado para usar, digamos, *N* threads.</span><span class="sxs-lookup"><span data-stu-id="811d9-119">Suppose that you have a single-processor computer that has been configured to use, say,  *N*  threads.</span></span> <span data-ttu-id="811d9-120">Suponha que uma planilha está sendo executado se torne um grande número de chamadas para uma função XLL que por sua vez envia uma solicitação de dados ou de um cálculo a ser executada em um servidor remoto ou de um cluster de servidores.</span><span class="sxs-lookup"><span data-stu-id="811d9-120">Suppose that a spreadsheet is running that makes a large number of calls to an XLL function that in turn sends a request for data or for a calculation to be performed to a remote server or cluster of servers.</span></span> <span data-ttu-id="811d9-121">Sujeito a topologia da árvore de dependência, Excel poderia chamar os tempos de função N quase simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="811d9-121">Subject to the topology of the dependency tree, Excel could call the function N times almost simultaneously.</span></span> <span data-ttu-id="811d9-122">Desde que o servidor ou servidores são suficientemente fast ou paralelo, o tempo de recálculo da planilha poderia ser reduzido em tanto quanto um fator de 1/s.</span><span class="sxs-lookup"><span data-stu-id="811d9-122">Provided that the server or servers are sufficiently fast or parallel, the recalculation time of the spreadsheet could be reduced by as much as a factor of 1/N.</span></span> 
  
<span data-ttu-id="811d9-123">A principal questão na escrita funções thread-safe está manipulando corretamente contenção de recursos.</span><span class="sxs-lookup"><span data-stu-id="811d9-123">The key issue in writing thread-safe functions is handling contention for resources correctly.</span></span> <span data-ttu-id="811d9-124">Isso geralmente significa contenção de memória, e ele pode ser dividido em dois problemas:</span><span class="sxs-lookup"><span data-stu-id="811d9-124">This usually means memory contention, and it can be broken down into two issues:</span></span>
  
- <span data-ttu-id="811d9-125">Como criar memória que você sabe que será usado apenas por esse segmento.</span><span class="sxs-lookup"><span data-stu-id="811d9-125">How to create memory that you know will only be used by this thread.</span></span>
    
- <span data-ttu-id="811d9-126">Como garantir que é acessada por vários threads memória compartilhada com segurança.</span><span class="sxs-lookup"><span data-stu-id="811d9-126">How to ensure that shared memory is accessed by multiple threads safely.</span></span>
    
<span data-ttu-id="811d9-127">A primeira coisa para estar ciente é quais tipos de memória em um XLL pode ser acessado por todos os threads e o que seja acessível apenas pelo thread atualmente em execução.</span><span class="sxs-lookup"><span data-stu-id="811d9-127">The first thing to be aware of is what memory in an XLL is accessible by all threads, and what is only accessible by the currently executing thread.</span></span>
  
 <span data-ttu-id="811d9-128">**Acessível por todos os threads**</span><span class="sxs-lookup"><span data-stu-id="811d9-128">**Accessible by all threads**</span></span>
  
- <span data-ttu-id="811d9-129">Variáveis, estruturas e instâncias da classe declarada fora o corpo de uma função.</span><span class="sxs-lookup"><span data-stu-id="811d9-129">Variables, structures, and class instances declared outside the body of a function.</span></span>
    
- <span data-ttu-id="811d9-130">Variáveis estáticas declaradas dentro do corpo de uma função.</span><span class="sxs-lookup"><span data-stu-id="811d9-130">Static variables declared within the body of a function.</span></span>
    
<span data-ttu-id="811d9-131">Nesses dois casos, a memória é definida reserve no bloco de memória da DLL criado para esta instância da DLL.</span><span class="sxs-lookup"><span data-stu-id="811d9-131">In these two cases, memory is set aside in the DLL's memory block created for this instance of the DLL.</span></span> <span data-ttu-id="811d9-132">Se outra instância do aplicativo carrega a DLL, ele obtém sua própria cópia de que a memória para que não haja nenhum contenção desses recursos de fora dessa instância da DLL.</span><span class="sxs-lookup"><span data-stu-id="811d9-132">If another application instance loads the DLL, it gets its own copy of that memory so that there is no contention for these resources from outside this instance of the DLL.</span></span>
  
 <span data-ttu-id="811d9-133">**Acessível somente pelo thread atual**</span><span class="sxs-lookup"><span data-stu-id="811d9-133">**Accessible only by the current thread**</span></span>
  
- <span data-ttu-id="811d9-134">Variáveis automáticas do código de função (incluindo argumentos da função).</span><span class="sxs-lookup"><span data-stu-id="811d9-134">Automatic variables within function code (including function arguments).</span></span>
    
<span data-ttu-id="811d9-135">Nesse caso, a memória é definida reserve na pilha para cada instância da chamada de função.</span><span class="sxs-lookup"><span data-stu-id="811d9-135">In this case, memory is set aside on the stack for each instance of the function call.</span></span>
  
> [!NOTE]
> <span data-ttu-id="811d9-136">O escopo de memória alocada dinamicamente depende do escopo do ponteiro do que aponta para ela: se o ponteiro pode ser acessado por todos os threads, a memória também será.</span><span class="sxs-lookup"><span data-stu-id="811d9-136">The scope of dynamically allocated memory depends on the scope of the pointer that points to it: if the pointer is accessible by all threads, the memory is also.</span></span> <span data-ttu-id="811d9-137">Se o ponteiro é uma variável automática em uma função, a memória alocada é efetivamente privada para esse segmento.</span><span class="sxs-lookup"><span data-stu-id="811d9-137">If the pointer is an automatic variable in a function, the allocated memory is effectively private to that thread.</span></span> 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a><span data-ttu-id="811d9-138">Memória acessível por apenas um segmento: memória Local de segmento</span><span class="sxs-lookup"><span data-stu-id="811d9-138">Memory Accessible by Only One Thread: Thread-Local Memory</span></span>

<span data-ttu-id="811d9-139">Visto que variáveis estáticas dentro do corpo de uma função são acessíveis por todos os threads, funções que usá-los não estão claramente thread-safe.</span><span class="sxs-lookup"><span data-stu-id="811d9-139">Given that static variables within the body of a function are accessible by all threads, functions that use them are clearly not thread safe.</span></span> <span data-ttu-id="811d9-140">Uma instância da função em um thread poderia ser a alteração do valor enquanto outra instância em outro thread é supondo que seja algo completamente diferente.</span><span class="sxs-lookup"><span data-stu-id="811d9-140">One instance of the function on one thread could be changing the value while another instance on another thread is assuming it is something completely different.</span></span> 
  
<span data-ttu-id="811d9-141">Existem duas razões para declarar variáveis estáticas dentro de uma função:</span><span class="sxs-lookup"><span data-stu-id="811d9-141">There are two reasons for declaring static variables within a function:</span></span>
  
1. <span data-ttu-id="811d9-142">Dados estáticos persistem de uma chamada para o próximo.</span><span class="sxs-lookup"><span data-stu-id="811d9-142">Static data persist from one call to the next.</span></span>
    
2. <span data-ttu-id="811d9-143">Um ponteiro para dados estáticos com segurança pode ser retornado pela função.</span><span class="sxs-lookup"><span data-stu-id="811d9-143">A pointer to static data can safely be returned by the function.</span></span>
    
<span data-ttu-id="811d9-144">No caso do primeiro motivo, talvez você queira ter dados que persiste e tem significado para todas as chamadas para a função: talvez um contador simple que é incrementado toda vez que a função for chamada em qualquer segmento, ou uma estrutura que coleta dados de uso e desempenho nos noite Ry chamada.</span><span class="sxs-lookup"><span data-stu-id="811d9-144">In the case of first reason, you might want to have data that persists and has meaning for all calls to the function: perhaps a simple counter that is incremented every time the function is called on any thread, or a structure that collects usage and performance data on every call.</span></span> <span data-ttu-id="811d9-145">A pergunta é como proteger os dados compartilhados ou uma estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="811d9-145">The question is how to protect the shared data or data structure.</span></span> <span data-ttu-id="811d9-146">Isso é feito melhor usando a seção crítica conforme a próxima seção explica.</span><span class="sxs-lookup"><span data-stu-id="811d9-146">This is best done by using critical section as the next section explains.</span></span>
  
<span data-ttu-id="811d9-147">Se os dados são destinados apenas para uso por este thread, que pode ser o caso por motivo 1 e é sempre o caso por motivo 2, a pergunta é como criar memória persiste, mas só está acessível a partir do thread.</span><span class="sxs-lookup"><span data-stu-id="811d9-147">If the data is intended only for use by this thread, which could be the case for reason 1 and is always the case for reason 2, the question is how to create memory that persists but is only accessible from this thread.</span></span> <span data-ttu-id="811d9-148">Uma solução é usar o armazenamento de thread local (TLS) API.</span><span class="sxs-lookup"><span data-stu-id="811d9-148">One solution is to use the thread-local storage (TLS) API.</span></span>
  
<span data-ttu-id="811d9-149">Por exemplo, considere uma função que retorna um ponteiro para um **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="811d9-149">For example, consider a function that returns a pointer to an **XLOPER**.</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

<span data-ttu-id="811d9-150">Essa função não é thread-safe porque um segmento pode retornar o estática **XLOPER12** enquanto outra é sobrescrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="811d9-150">This function is not thread safe because one thread can return the static **XLOPER12** while another is overwriting it.</span></span> <span data-ttu-id="811d9-151">A probabilidade disso acontecer é maior ainda se o **XLOPER12** precisa ser passado para **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="811d9-151">The likelihood of this happening is greater still if the **XLOPER12** needs to be passed to **xlAutoFree12**.</span></span> <span data-ttu-id="811d9-152">Uma solução é alocar **XLOPER12**, retornar um ponteiro para ele e implementar **xlAutoFree12** para que a memória **XLOPER12** propriamente dito é liberada.</span><span class="sxs-lookup"><span data-stu-id="811d9-152">One solution is to allocate an **XLOPER12**, return a pointer to it, and implement **xlAutoFree12** so that the **XLOPER12** memory itself is freed.</span></span> <span data-ttu-id="811d9-153">Essa abordagem é usada em muitas das funções de exemplo mostradas no [Gerenciamento de memória no Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="811d9-153">This approach is used in many of the example functions shown in [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

<span data-ttu-id="811d9-154">Essa abordagem é mais simples implementar que a abordagem descrita na próxima seção, que utiliza a API de TLS, mas ele tem algumas desvantagens.</span><span class="sxs-lookup"><span data-stu-id="811d9-154">This approach is simpler to implement than the approach outlined in the next section, which relies on the TLS API, but it has some disadvantages.</span></span> <span data-ttu-id="811d9-155">Em primeiro lugar, o Excel deve chamar **xlAutoFree**/ **xlAutoFree12** seja qual for o tipo de retornado **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="811d9-155">First, Excel must call **xlAutoFree**/ **xlAutoFree12** whatever the type of the returned **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="811d9-156">Segundo, há um problema ao retornar **XLOPER**/ **XLOPER12**s são o valor de retorno de uma chamada a uma função de retorno de chamada da API C.</span><span class="sxs-lookup"><span data-stu-id="811d9-156">Second, there is a problem when returning **XLOPER**/ **XLOPER12**s that are the return value of a call to a C API callback function.</span></span> <span data-ttu-id="811d9-157">**XLOPER**/ **XLOPER12** podem apontar para memória que precisa ser liberado pelo Excel, mas **XLOPER**/ **XLOPER12** propriamente dito deve ser liberado da mesma forma que ela foi alocada.</span><span class="sxs-lookup"><span data-stu-id="811d9-157">The **XLOPER**/ **XLOPER12** may point to memory that needs to be freed by Excel, but the **XLOPER**/ **XLOPER12** itself must be freed in the same way it was allocated.</span></span> <span data-ttu-id="811d9-158">Se tais **XLOPER**/ **XLOPER12** deve ser usado como o valor de retorno de uma função de planilha XLL, há um meio fácil para informar aos **xlAutoFree**/ **xlAutoFree12** da necessidade de livre ambos os ponteiros da maneira apropriada.</span><span class="sxs-lookup"><span data-stu-id="811d9-158">If such an **XLOPER**/ **XLOPER12** is to be used as the return value of an XLL worksheet function, there is no easy way to inform **xlAutoFree**/ **xlAutoFree12** of the need to free both pointers in the appropriate way.</span></span> <span data-ttu-id="811d9-159">(Definindo o **xlbitXLFree** e o **xlbitDLLFree** não resolve o problema, conforme o tratamento de **XLOPER/XLOPER12s** no Excel com ambos os conjunto é indefinido e pode ser alterado de versão para versão.) Para contornar esse problema, XLL pode fazer cópias profundas de todos os alocadas Excel **XLOPER/XLOPER12s** que ele retorna à planilha.</span><span class="sxs-lookup"><span data-stu-id="811d9-159">(Setting both the **xlbitXLFree** and **xlbitDLLFree** does not solve the problem, as the treatment of **XLOPER/XLOPER12s** in Excel with both set is undefined and might change from version to version.) To work around this problem, the XLL can make deep copies of all Excel-allocated **XLOPER/XLOPER12s** that it returns to the worksheet.</span></span> 
  
<span data-ttu-id="811d9-160">Uma solução que evita essas limitações é preencher e retornar um segmento local **XLOPER/XLOPER12**, uma abordagem que necessita desse **xlAutoFree/xlAutoFree12** não libera o ponteiro **XLOPER/XLOPER12** em si.</span><span class="sxs-lookup"><span data-stu-id="811d9-160">A solution that avoids these limitations is to populate and return a thread-local **XLOPER/XLOPER12**, an approach that necessitates that **xlAutoFree/xlAutoFree12** does not free the **XLOPER/XLOPER12** pointer itself.</span></span> 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

<span data-ttu-id="811d9-161">A próxima pergunta é como configurar e recuperar a memória de segmento locais, em outras palavras, como implementar a função **get_thread_local_xloper12** no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="811d9-161">The next question is how to set up and retrieve the thread-local memory, in other words, how to implement the function **get_thread_local_xloper12** in the previous example.</span></span> <span data-ttu-id="811d9-162">Isso é feito usando o Thread TLS (armazenamento Local) API.</span><span class="sxs-lookup"><span data-stu-id="811d9-162">This is done using the Thread Local Storage (TLS) API.</span></span> <span data-ttu-id="811d9-163">A primeira etapa é obter um índice TLS usando o **TlsAlloc**, que basicamente deve ser lançada usando **TlsFree**.</span><span class="sxs-lookup"><span data-stu-id="811d9-163">The first step is to obtain a TLS index by using **TlsAlloc**, which must ultimately be released using **TlsFree**.</span></span> <span data-ttu-id="811d9-164">Ambas são melhor realizadas a partir da **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="811d9-164">Both are best accomplished from **DllMain**.</span></span>
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

<span data-ttu-id="811d9-165">Depois de obter o índice, a próxima etapa é alocar um bloco de memória para cada segmento.</span><span class="sxs-lookup"><span data-stu-id="811d9-165">After you obtain the index, the next step is to allocate a block of memory for each thread.</span></span> <span data-ttu-id="811d9-166">A [Documentação de desenvolvimento do Windows](http://msdn.microsoft.com/pt-br/library/ms682583%28VS.85%29.aspx) recomenda fazer isso sempre que a função de retorno de chamada **DllMain** é chamada com um evento **DLL_THREAD_ATTACH** e liberar a memória em cada **DLL_THREAD_DETACH**.</span><span class="sxs-lookup"><span data-stu-id="811d9-166">The [Windows Development Documentation](http://msdn.microsoft.com/pt-br/library/ms682583%28VS.85%29.aspx) recommends doing this every time the **DllMain** callback function is called with a **DLL_THREAD_ATTACH** event, and freeing the memory on every **DLL_THREAD_DETACH**.</span></span> <span data-ttu-id="811d9-167">No entanto, seguir este conselhos causaria sua DLL fazer trabalho desnecessário para threads não é usado para o recálculo.</span><span class="sxs-lookup"><span data-stu-id="811d9-167">However, following this advice would cause your DLL to do unnecessary work for threads not used for recalculation.</span></span> 
  
<span data-ttu-id="811d9-168">Em vez disso, é melhor usar uma estratégia de alocação no primeiro uso.</span><span class="sxs-lookup"><span data-stu-id="811d9-168">Instead, it is better to use an allocate-on-first-use strategy.</span></span> <span data-ttu-id="811d9-169">Primeiro, você precisará definir uma estrutura que você deseja alocar para cada segmento.</span><span class="sxs-lookup"><span data-stu-id="811d9-169">First, you need to define a structure that you want to allocate for each thread.</span></span> <span data-ttu-id="811d9-170">Para os exemplos anteriores que retornam **XLOPERs** ou **XLOPER12s**, o seguinte é suficiente, mas você pode criar qualquer estrutura que atenda às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="811d9-170">For the previous examples that return **XLOPERs** or **XLOPER12s**, the following suffices, but you can create any structure that satisfies your needs.</span></span>
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

<span data-ttu-id="811d9-171">A função a seguir obtém um ponteiro para a instância do segmento local ou aloca um destes se esta for a primeira chamada.</span><span class="sxs-lookup"><span data-stu-id="811d9-171">The following function gets a pointer to the thread-local instance, or allocates one if this is the first call.</span></span>
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

<span data-ttu-id="811d9-172">Agora você pode ver como a memória do segmento local **XLOPER/XLOPER12** é obtida: primeiro, você obtém um ponteiro para a instância do segmento de **TLS_data**e, em seguida, você retorna um ponteiro para **XLOPER/XLOPER12** contidos nela, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="811d9-172">Now you can see how the thread-local **XLOPER/XLOPER12** memory is obtained: first, you get a pointer to the thread's instance of **TLS_data**, and then you return a pointer to the **XLOPER/XLOPER12** contained within it, as follows.</span></span> 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

<span data-ttu-id="811d9-173">As funções **mtr_safe_example_1** e **mtr_safe_example_2** podem ser registradas como funções de planilha de thread-safe quando você estiver executando o Excel.</span><span class="sxs-lookup"><span data-stu-id="811d9-173">The **mtr_safe_example_1** and **mtr_safe_example_2** functions can be registered as thread-safe worksheet functions when you are running Excel.</span></span> <span data-ttu-id="811d9-174">No entanto, você não pode misturar as duas abordagens em um XLL.</span><span class="sxs-lookup"><span data-stu-id="811d9-174">However, you cannot mix the two approaches in one XLL.</span></span> <span data-ttu-id="811d9-175">Seu XLL só pode exportar uma implementação do **xlAutoFree** e **xlAutoFree12**e cada estratégia de memória exige uma abordagem diferente.</span><span class="sxs-lookup"><span data-stu-id="811d9-175">Your XLL can only export one implementation of **xlAutoFree** and **xlAutoFree12**, and each memory strategy requires a different approach.</span></span> <span data-ttu-id="811d9-176">Com **mtr_safe_example_1**, o ponteiro passado **xlAutoFree/xlAutoFree12** deve ser liberado junto com quaisquer dados para que ela aponta.</span><span class="sxs-lookup"><span data-stu-id="811d9-176">With **mtr_safe_example_1**, the pointer passed to **xlAutoFree/xlAutoFree12** must be freed along with any data it points to.</span></span> <span data-ttu-id="811d9-177">Com **mtr_safe_example_2**, somente os dados apontado para devem ser liberados.</span><span class="sxs-lookup"><span data-stu-id="811d9-177">With **mtr_safe_example_2**, only the pointed-to data should be freed.</span></span>
  
<span data-ttu-id="811d9-178">Windows também fornece uma função **GetCurrentThreadId**, que retorna a ID exclusivo em todo o sistema. do thread atual</span><span class="sxs-lookup"><span data-stu-id="811d9-178">Windows also provides a function **GetCurrentThreadId**, which returns the current thread's unique system-wide ID.</span></span> <span data-ttu-id="811d9-179">Isso oferece o desenvolvedor com outra maneira para tornar o thread de código seguros ou fazer seu thread de comportamento específico.</span><span class="sxs-lookup"><span data-stu-id="811d9-179">This provides the developer with another way to make code thread safe, or to make its behavior thread specific.</span></span>
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a><span data-ttu-id="811d9-180">Memória acessível somente por mais de um segmento: seções críticas</span><span class="sxs-lookup"><span data-stu-id="811d9-180">Memory Accessible Only by More than One Thread: Critical Sections</span></span>

<span data-ttu-id="811d9-181">Você deve proteger memória de leitura/gravação que possa ser acessada por mais de um segmento usando as seções críticas.</span><span class="sxs-lookup"><span data-stu-id="811d9-181">You should protect read/write memory that can be accessed by more than one thread using critical sections.</span></span> <span data-ttu-id="811d9-182">Você precisa de uma seção crítica nomeada para cada bloco de memória que você queira proteger.</span><span class="sxs-lookup"><span data-stu-id="811d9-182">You need a named critical section for each block of memory you want to protect.</span></span> <span data-ttu-id="811d9-183">Você pode inicializá-los durante a chamada para a função **xlAutoOpen** e liberá-los e defini-las como null durante a chamada para a função **xlAutoClose** .</span><span class="sxs-lookup"><span data-stu-id="811d9-183">You can initialize these during the call to the **xlAutoOpen** function, and release them and set them to null during the call to the **xlAutoClose** function.</span></span> <span data-ttu-id="811d9-184">Em seguida, você precisa conter cada acesso ao bloco protegido dentro de um par de chamadas para **EnterCriticalSection** e **LeaveCriticalSection**.</span><span class="sxs-lookup"><span data-stu-id="811d9-184">You then need to contain each access to the protected block within a pair of calls to **EnterCriticalSection** and **LeaveCriticalSection**.</span></span> <span data-ttu-id="811d9-185">Apenas um segmento tem permissão para a seção crítica a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="811d9-185">Only one thread is permitted into the critical section at any time.</span></span> <span data-ttu-id="811d9-186">Aqui está um exemplo de como a inicialização, desinicialização e uso de uma seção chamada **g_csSharedTable**.</span><span class="sxs-lookup"><span data-stu-id="811d9-186">Here is an example of the initialization, uninitialization, and use of a section called **g_csSharedTable**.</span></span>
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

<span data-ttu-id="811d9-187">Talvez mais segura, de outra maneira de proteger um bloco de memória é criar uma classe que contém sua própria **CRITICAL_SECTION** e cujos construtor, destrutor e métodos accessor cuidam de seu uso.</span><span class="sxs-lookup"><span data-stu-id="811d9-187">Another, perhaps safer way of protecting a block of memory is to create a class that contains its own **CRITICAL_SECTION** and whose constructor, destructor, and accessor methods take care of its use.</span></span> <span data-ttu-id="811d9-188">Essa abordagem tem a vantagem adicional de proteger os objetos que podem ser inicializados antes **xlAutoOpen** seja executado ou sobreviver depois **xlAutoClose** é chamado, mas você deve tomar cuidado sobre a criação de muitas seções críticas e o sistema operacional sobrecarga que isso seria criar.</span><span class="sxs-lookup"><span data-stu-id="811d9-188">This approach has the added advantage of protecting objects that may be initialized before **xlAutoOpen** is run, or survive after **xlAutoClose** is called, but you should be careful about creating too many critical sections and the operating system overhead that this would create.</span></span> 
  
<span data-ttu-id="811d9-189">Quando você tem o código que precisa acessar mais de um bloco de memória protegida ao mesmo tempo, você precisa considerar com muito cuidado a ordem na qual as seções críticas entra e sai.</span><span class="sxs-lookup"><span data-stu-id="811d9-189">When you have code that needs access to more than one block of protected memory at the same time, you need to consider very carefully the order in which the critical sections are entered and exited.</span></span> <span data-ttu-id="811d9-190">Por exemplo, duas funções a seguir poderiam criar um bloqueio.</span><span class="sxs-lookup"><span data-stu-id="811d9-190">For example, the following two functions could create a deadlock.</span></span>
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

<span data-ttu-id="811d9-191">Se a primeira função de um segmento entra **g_csSharedTableA** enquanto o segundo em outro thread entra **g_csSharedTableB**, ambos os threads paralisar.</span><span class="sxs-lookup"><span data-stu-id="811d9-191">If the first function on one thread enters **g_csSharedTableA** while the second on another thread enters **g_csSharedTableB**, both threads hang.</span></span> <span data-ttu-id="811d9-192">A abordagem correta é entrar em uma ordem consistente e sair na ordem inversa, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="811d9-192">The correct approach is to enter in a consistent order and exit in the reverse order, as follows.</span></span>
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

<span data-ttu-id="811d9-193">Onde for possível, é melhor do thread co-operation ponto de vista para isolar o acesso a blocos distintos, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="811d9-193">Where possible, it is better from a thread co-operation point of view to isolate access to distinct blocks, as shown here.</span></span>
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

<span data-ttu-id="811d9-194">Onde há muita contenção para um recurso compartilhado, como solicitações de acesso de curta duração frequente, você deve considerar usando a capacidade da seção críticos para rotação.</span><span class="sxs-lookup"><span data-stu-id="811d9-194">Where there is a lot of contention for a shared resource, such as frequent short-duration access requests, you should consider using the critical section's ability to spin.</span></span> <span data-ttu-id="811d9-195">Essa é uma técnica que torna a espera pelo recurso menos intensivos de processador.</span><span class="sxs-lookup"><span data-stu-id="811d9-195">This is a technique that makes waiting for the resource less processor-intensive.</span></span> <span data-ttu-id="811d9-196">Para fazer isso, você pode usar qualquer um dos **InitializeCriticalSectionAndSpinCount** ao inicializar a seção ou **SetCriticalSectionSpinCount** inicializado uma vez, para definir o número de vezes que o thread faz um loop antes de aguardar recursos se tornarem disponível.</span><span class="sxs-lookup"><span data-stu-id="811d9-196">To do this, you can use either **InitializeCriticalSectionAndSpinCount** when initializing the section or **SetCriticalSectionSpinCount** once initialized, to set the number of times the thread loops before waiting for resources to become available.</span></span> <span data-ttu-id="811d9-197">A operação de espera é cara, portanto a rotação evita isso se o recurso for liberado enquanto isso.</span><span class="sxs-lookup"><span data-stu-id="811d9-197">The wait operation is expensive, so spinning avoids this if the resource is freed in the meantime.</span></span> <span data-ttu-id="811d9-198">Em um sistema de processador único, a contagem de rotações é efetivamente ignorada, mas você ainda pode especificá-lo sem causar nenhum dano.</span><span class="sxs-lookup"><span data-stu-id="811d9-198">On a single processor system, the spin count is effectively ignored, but you can still specify it without doing any harm.</span></span> <span data-ttu-id="811d9-199">O Gerenciador de heap de memória utiliza uma contagem de rotação de 4000.</span><span class="sxs-lookup"><span data-stu-id="811d9-199">The memory heap manager uses a spin count of 4000.</span></span> <span data-ttu-id="811d9-200">Para obter mais informações sobre o uso das seções críticas, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="811d9-200">For more information about the use of critical sections, see the Windows SDK documentation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="811d9-201">Confira também</span><span class="sxs-lookup"><span data-stu-id="811d9-201">See also</span></span>



[<span data-ttu-id="811d9-202">Gerenciamento de memória no Excel</span><span class="sxs-lookup"><span data-stu-id="811d9-202">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="811d9-203">Recálculo multithreaded no Excel</span><span class="sxs-lookup"><span data-stu-id="811d9-203">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="811d9-204">Gerenciador de suplemento e funções da Interface XLL</span><span class="sxs-lookup"><span data-stu-id="811d9-204">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

