---
title: Multithreading e contenção de memória no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- multithreading no excel, contenção de memória no Excel, funções [Excel 2007], thread-safe, funções thread-safe [Excel 2007], memória local de threads [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Aplicável a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301635"
---
# <a name="multithreading-and-memory-contention-in-excel"></a><span data-ttu-id="48491-104">Multithreading e contenção de memória no Excel</span><span class="sxs-lookup"><span data-stu-id="48491-104">Multithreading and Memory Contention in Excel</span></span>

 <span data-ttu-id="48491-105">**Aplicável a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="48491-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="48491-106">Versões do Microsoft Excel anteriores ao Excel 2007 usam um único thread para todos os cálculos de planilha.</span><span class="sxs-lookup"><span data-stu-id="48491-106">Versions of Microsoft Excel earlier than Excel 2007 use a single thread for all worksheet calculations.</span></span> <span data-ttu-id="48491-107">No entanto, a partir do Excel 2007, o Excel pode ser configurado para usar de 1 a 1024 threads simultâneos para o cálculo de planilhas.</span><span class="sxs-lookup"><span data-stu-id="48491-107">However, starting in Excel 2007, Excel can be configured to use from 1 to 1024 concurrent threads for worksheet calculation.</span></span> <span data-ttu-id="48491-108">Em um computador com vários processadores ou vários núcleos, o número padrão de threads é igual ao número de processadores ou núcleos.</span><span class="sxs-lookup"><span data-stu-id="48491-108">On a multi-processor or multi-core computer, the default number of threads is equal to the number of processors or cores.</span></span> <span data-ttu-id="48491-109">Portanto, células thread-safe, ou células que contenham apenas funções que são thread-safe, podem ser alocadas a threads simultâneos, sujeitas à lógica de recálculo comum que estabelece que elas precisam ser calculadas após seus precedentes.</span><span class="sxs-lookup"><span data-stu-id="48491-109">Therefore, thread-safe cells, or cells that only contain functions that are thread safe, can be allotted to concurrent threads, subject to the usual recalculation logic of needing to be calculated after their precedents.</span></span>
  
## <a name="thread-safe-functions"></a><span data-ttu-id="48491-110">Funções thread-safe</span><span class="sxs-lookup"><span data-stu-id="48491-110">Thread-Safe Functions</span></span>

<span data-ttu-id="48491-111">A maioria das funções de planilha internas, a partir do Excel 2007, são thread-safe.</span><span class="sxs-lookup"><span data-stu-id="48491-111">Most of the built-in worksheet functions starting in Excel 2007 are thread safe.</span></span> <span data-ttu-id="48491-112">Você também pode gravar e registrar funções XLL como sendo thread-safe.</span><span class="sxs-lookup"><span data-stu-id="48491-112">You can also write and register XLL functions as being thread safe.</span></span> <span data-ttu-id="48491-113">O Excel usa um thread (seu thread principal) para chamar todos os comandos, funções não thread-safe, funções **xlAuto** (exceto [xlAutoFree](xlautofree-xlautofree12.md) e **xlAutoFree12**) e funções COM e do Visual Basic for Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="48491-113">Excel uses one thread (its main thread) to call all commands, thread-unsafe functions, **xlAuto** functions (except [xlAutoFree](xlautofree-xlautofree12.md) and **xlAutoFree12**), and COM and Visual Basic for Applications (VBA) functions.</span></span>
  
<span data-ttu-id="48491-114">Quando uma função XLL retorna **XLOPER** ou **XLOPER12** com o conjunto **xlbitDLLFree**, o Excel usa o mesmo de thread no qual a chamada de função foi feita para chamar **xlAutoFree** ou **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="48491-114">Where an XLL function returns an **XLOPER** or **XLOPER12** with **xlbitDLLFree** set, Excel uses the same thread on which the function call was made to call **xlAutoFree** or **xlAutoFree12**.</span></span> <span data-ttu-id="48491-115">A chamada para **xlAutoFree** ou **xlAutoFree12** é feita antes da próxima chamada de função nesse thread.</span><span class="sxs-lookup"><span data-stu-id="48491-115">The call to **xlAutoFree** or **xlAutoFree12** is made before the next function call on that thread.</span></span> 
  
<span data-ttu-id="48491-116">Para desenvolvedores de XLL, há benefícios para a criação de funções thread-safe:</span><span class="sxs-lookup"><span data-stu-id="48491-116">For XLL developers, there are benefits for creating thread-safe functions:</span></span>
  
- <span data-ttu-id="48491-117">Elas permitem que o Excel tire o máximo de proveito de um computador com vários processadores ou vários núcleos.</span><span class="sxs-lookup"><span data-stu-id="48491-117">They allow Excel to make the most of a multi-processor or multi-core computer.</span></span>
    
- <span data-ttu-id="48491-118">Elas abrem a possibilidade de usar servidores remotos com muito mais eficiência do que pode ser feito usando um único thread.</span><span class="sxs-lookup"><span data-stu-id="48491-118">They open up the possibility of using remote servers much more efficiently than can be done using a single thread.</span></span>
    
<span data-ttu-id="48491-119">Suponha que você tenha um computador com processador único que tenha sido configurado para usar *N* threads.</span><span class="sxs-lookup"><span data-stu-id="48491-119">Suppose that you have a single-processor computer that has been configured to use, say,  *N*  threads.</span></span> <span data-ttu-id="48491-120">Imagine uma planilha em execução que faz um grande número de chamadas para uma função XLL que, por sua vez, envia uma solicitação de dados ou de cálculo a um servidor remoto ou cluster de servidores.</span><span class="sxs-lookup"><span data-stu-id="48491-120">Suppose that a spreadsheet is running that makes a large number of calls to an XLL function that in turn sends a request for data or for a calculation to be performed to a remote server or cluster of servers.</span></span> <span data-ttu-id="48491-121">Dependendo da topologia da árvore de dependência, o Excel pode chamar a função N vezes quase simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="48491-121">Subject to the topology of the dependency tree, Excel could call the function N times almost simultaneously.</span></span> <span data-ttu-id="48491-122">Desde que o servidor ou os servidores sejam suficientemente rápidos ou paralelos, o tempo de recálculo da planilha pode ser reduzido até um fator de 1/N.</span><span class="sxs-lookup"><span data-stu-id="48491-122">Provided that the server or servers are sufficiently fast or parallel, the recalculation time of the spreadsheet could be reduced by as much as a factor of 1/N.</span></span> 
  
<span data-ttu-id="48491-123">O principal problema na gravação de funções thread-safe é manipular a contenção de recursos corretamente.</span><span class="sxs-lookup"><span data-stu-id="48491-123">The key issue in writing thread-safe functions is handling contention for resources correctly.</span></span> <span data-ttu-id="48491-124">Isso geralmente significa contenção de memória e pode ser dividido em dois problemas:</span><span class="sxs-lookup"><span data-stu-id="48491-124">This usually means memory contention, and it can be broken down into two issues:</span></span>
  
- <span data-ttu-id="48491-125">Como criar a memória que você sabe que só será usada por esse thread.</span><span class="sxs-lookup"><span data-stu-id="48491-125">How to create memory that you know will only be used by this thread.</span></span>
    
- <span data-ttu-id="48491-126">Como garantir que a memória compartilhada seja acessada por vários threads com segurança.</span><span class="sxs-lookup"><span data-stu-id="48491-126">How to ensure that shared memory is accessed by multiple threads safely.</span></span>
    
<span data-ttu-id="48491-127">A primeira coisa a ter em conta é qual memória em um XLL é acessível por todos os encadeamentos e qual é acessível apenas pelo encadeamento atualmente em execução.</span><span class="sxs-lookup"><span data-stu-id="48491-127">The first thing to be aware of is what memory in an XLL is accessible by all threads, and what is only accessible by the currently executing thread.</span></span>
  
 <span data-ttu-id="48491-128">**Acessível por todos os threads**</span><span class="sxs-lookup"><span data-stu-id="48491-128">**Accessible by all threads**</span></span>
  
- <span data-ttu-id="48491-129">Variáveis, estruturas e instâncias de classes declaradas fora do corpo de uma função.</span><span class="sxs-lookup"><span data-stu-id="48491-129">Variables, structures, and class instances declared outside the body of a function.</span></span>
    
- <span data-ttu-id="48491-130">Variáveis estáticas declaradas no corpo de uma função.</span><span class="sxs-lookup"><span data-stu-id="48491-130">Static variables declared within the body of a function.</span></span>
    
<span data-ttu-id="48491-131">Nesses dois casos, a memória é reservada no bloco de memória da DLL criado para essa instância da DLL.</span><span class="sxs-lookup"><span data-stu-id="48491-131">In these two cases, memory is set aside in the DLL's memory block created for this instance of the DLL.</span></span> <span data-ttu-id="48491-132">Se outra instância de aplicativo carregar a DLL, ela obterá sua própria cópia dessa memória para que não haja contenção desses recursos de fora dessa instância da DLL.</span><span class="sxs-lookup"><span data-stu-id="48491-132">If another application instance loads the DLL, it gets its own copy of that memory so that there is no contention for these resources from outside this instance of the DLL.</span></span>
  
 <span data-ttu-id="48491-133">**Acessível apenas pelo thread atual**</span><span class="sxs-lookup"><span data-stu-id="48491-133">**Accessible only by the current thread**</span></span>
  
- <span data-ttu-id="48491-134">Variáveis automáticas no código de função (incluindo argumentos de função).</span><span class="sxs-lookup"><span data-stu-id="48491-134">Automatic variables within function code (including function arguments).</span></span>
    
<span data-ttu-id="48491-135">Nesse caso, a memória é reservada na pilha para cada instância da chamada de função.</span><span class="sxs-lookup"><span data-stu-id="48491-135">In this case, memory is set aside on the stack for each instance of the function call.</span></span>
  
> [!NOTE]
> <span data-ttu-id="48491-136">O escopo da memória alocada dinamicamente depende do escopo do ponteiro que aponta para ela: se o ponteiro for acessível por todos os threads, o mesmo acontecerá com a memória.</span><span class="sxs-lookup"><span data-stu-id="48491-136">The scope of dynamically allocated memory depends on the scope of the pointer that points to it: if the pointer is accessible by all threads, the memory is also.</span></span> <span data-ttu-id="48491-137">Se o ponteiro for uma variável automática em uma função, a memória alocada será efetivamente privada para esse segmento.</span><span class="sxs-lookup"><span data-stu-id="48491-137">If the pointer is an automatic variable in a function, the allocated memory is effectively private to that thread.</span></span> 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a><span data-ttu-id="48491-138">Memória acessível por apenas um thread: memória local de thread</span><span class="sxs-lookup"><span data-stu-id="48491-138">Memory Accessible by Only One Thread: Thread-Local Memory</span></span>

<span data-ttu-id="48491-139">Considerando que as variáveis estáticas dentro do corpo de uma função são acessíveis por todos os threads, as funções que as utilizam claramente não são thread-safe.</span><span class="sxs-lookup"><span data-stu-id="48491-139">Given that static variables within the body of a function are accessible by all threads, functions that use them are clearly not thread safe.</span></span> <span data-ttu-id="48491-140">Uma instância da função em um thread pode estar alterando o valor, enquanto outra instância em outro thread está assumindo que se trata de algo completamente diferente.</span><span class="sxs-lookup"><span data-stu-id="48491-140">One instance of the function on one thread could be changing the value while another instance on another thread is assuming it is something completely different.</span></span> 
  
<span data-ttu-id="48491-141">Existem duas razões para declarar variáveis estáticas dentro de uma função:</span><span class="sxs-lookup"><span data-stu-id="48491-141">There are two reasons for declaring static variables within a function:</span></span>
  
1. <span data-ttu-id="48491-142">Dados estáticos persistem de uma chamada para a seguinte.</span><span class="sxs-lookup"><span data-stu-id="48491-142">Static data persist from one call to the next.</span></span>
    
2. <span data-ttu-id="48491-143">Um ponteiro para dados estáticos pode ser retornado com segurança pela função.</span><span class="sxs-lookup"><span data-stu-id="48491-143">A pointer to static data can safely be returned by the function.</span></span>
    
<span data-ttu-id="48491-144">No caso do primeiro motivo, talvez você queira ter dados que persistam e tenham significado para todas as chamadas à função: talvez um contador simples que seja incrementado toda vez que a função for chamada em qualquer thread ou uma estrutura que colete dados de uso e desempenho em todas as chamadas.</span><span class="sxs-lookup"><span data-stu-id="48491-144">In the case of first reason, you might want to have data that persists and has meaning for all calls to the function: perhaps a simple counter that is incremented every time the function is called on any thread, or a structure that collects usage and performance data on every call.</span></span> <span data-ttu-id="48491-145">A questão é como proteger os dados compartilhados ou a estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="48491-145">The question is how to protect the shared data or data structure.</span></span> <span data-ttu-id="48491-146">Isso é feito da melhor maneira usando a seção crítica, como a próxima seção explica.</span><span class="sxs-lookup"><span data-stu-id="48491-146">This is best done by using critical section as the next section explains.</span></span>
  
<span data-ttu-id="48491-147">Se os dados se destinam apenas ao uso por esse thread, o que pode ser o caso do motivo 1 e é sempre o caso do motivo 2, a questão é como criar uma memória que persista, mas que apenas seja acessível por esse thread.</span><span class="sxs-lookup"><span data-stu-id="48491-147">If the data is intended only for use by this thread, which could be the case for reason 1 and is always the case for reason 2, the question is how to create memory that persists but is only accessible from this thread.</span></span> <span data-ttu-id="48491-148">Uma solução é usar a API de armazenamento local de thread (TLS).</span><span class="sxs-lookup"><span data-stu-id="48491-148">One solution is to use the thread-local storage (TLS) API.</span></span>
  
<span data-ttu-id="48491-149">Por exemplo, considere uma função que retorne um ponteiro para um **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="48491-149">For example, consider a function that returns a pointer to an **XLOPER**.</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

<span data-ttu-id="48491-150">Essa função não é thread-safe, pois um thread pode retornar o **XLOPER12** estático enquanto outro o sobrescreve.</span><span class="sxs-lookup"><span data-stu-id="48491-150">This function is not thread safe because one thread can return the static **XLOPER12** while another is overwriting it.</span></span> <span data-ttu-id="48491-151">A probabilidade de isso acontecer será ainda maior se for necessário transmitir **XLOPER12** para **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="48491-151">The likelihood of this happening is greater still if the **XLOPER12** needs to be passed to **xlAutoFree12**.</span></span> <span data-ttu-id="48491-152">Uma solução é alocar um **XLOPER12**, retornar um ponteiro para ele e implementar **xlAutoFree12** para que a memória de **XLOPER12** propriamente dita seja liberada.</span><span class="sxs-lookup"><span data-stu-id="48491-152">One solution is to allocate an **XLOPER12**, return a pointer to it, and implement **xlAutoFree12** so that the **XLOPER12** memory itself is freed.</span></span> <span data-ttu-id="48491-153">Essa abordagem é usada em muitas das funções de exemplo mostradas em [Gerenciamento da memória no Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="48491-153">This approach is used in many of the example functions shown in [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
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

<span data-ttu-id="48491-154">Essa abordagem é mais simples de implementar do que a abordagem descrita na próxima seção, que se baseia na API TLS, mas apresenta algumas desvantagens.</span><span class="sxs-lookup"><span data-stu-id="48491-154">This approach is simpler to implement than the approach outlined in the next section, which relies on the TLS API, but it has some disadvantages.</span></span> <span data-ttu-id="48491-155">Primeiro, o Excel deve chamar **xlAutoFree**/ **xlAutoFree12** seja qual for o tipo do **XLOPER**/ **XLOPER12** retornado.</span><span class="sxs-lookup"><span data-stu-id="48491-155">First, Excel must call **xlAutoFree**/ **xlAutoFree12** whatever the type of the returned **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="48491-156">Em segundo lugar, há um problema ao retornar **XLOPER**/ **XLOPER12**s que são o valor de retorno de uma chamada para uma função de retorno de chamada da API C.</span><span class="sxs-lookup"><span data-stu-id="48491-156">Second, there is a problem when returning **XLOPER**/ **XLOPER12**s that are the return value of a call to a C API callback function.</span></span> <span data-ttu-id="48491-157">O **XLOPER**/ **XLOPER12** pode apontar para uma memória que precisa ser liberada pelo Excel, mas o **XLOPER**/ **XLOPER12** propriamente dito deve ser liberado da mesma maneira com que foi alocado.</span><span class="sxs-lookup"><span data-stu-id="48491-157">The **XLOPER**/ **XLOPER12** may point to memory that needs to be freed by Excel, but the **XLOPER**/ **XLOPER12** itself must be freed in the same way it was allocated.</span></span> <span data-ttu-id="48491-158">Se esse **XLOPER**/ **XLOPER12** tiver que ser usado como o valor de retorno de uma função de planilha XLL, não existe uma maneira fácil de informar **xlAutoFree**/ **xlAutoFree12** sobre a necessidade de liberar ambos os ponteiros da maneira apropriada.</span><span class="sxs-lookup"><span data-stu-id="48491-158">If such an **XLOPER**/ **XLOPER12** is to be used as the return value of an XLL worksheet function, there is no easy way to inform **xlAutoFree**/ **xlAutoFree12** of the need to free both pointers in the appropriate way.</span></span> <span data-ttu-id="48491-159">(Definir **xlbitXLFree** e **xlbitDLLFree** não resolve o problema, pois o tratamento de **XLOPER/XLOPER12s** no Excel com ambos configurados é indefinido e pode mudar de versão para versão.) Para contornar esse problema, o XLL pode fazer cópias profundas de todos os **XLOPER/XLOPER12s** alocados pelo Excel que ele retorna à planilha.</span><span class="sxs-lookup"><span data-stu-id="48491-159">(Setting both the **xlbitXLFree** and **xlbitDLLFree** does not solve the problem, as the treatment of **XLOPER/XLOPER12s** in Excel with both set is undefined and might change from version to version.) To work around this problem, the XLL can make deep copies of all Excel-allocated **XLOPER/XLOPER12s** that it returns to the worksheet.</span></span> 
  
<span data-ttu-id="48491-160">Uma solução que evita essas limitações é preencher e retornar um **XLOPER/XLOPER12** local de thread, uma abordagem que exige que **xlAutoFree/xlAutoFree12** não libere o próprio ponteiro **XLOPER/XLOPER12** propriamente dito.</span><span class="sxs-lookup"><span data-stu-id="48491-160">A solution that avoids these limitations is to populate and return a thread-local **XLOPER/XLOPER12**, an approach that necessitates that **xlAutoFree/xlAutoFree12** does not free the **XLOPER/XLOPER12** pointer itself.</span></span> 
  
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

<span data-ttu-id="48491-161">A próxima pergunta é como configurar e recuperar a memória local de thread, em outras palavras, como implementar a função **get_thread_local_xloper12** no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="48491-161">The next question is how to set up and retrieve the thread-local memory, in other words, how to implement the function **get_thread_local_xloper12** in the previous example.</span></span> <span data-ttu-id="48491-162">Isso é feito usando a API TLS (Armazenamento Local de Thread).</span><span class="sxs-lookup"><span data-stu-id="48491-162">This is done using the Thread Local Storage (TLS) API.</span></span> <span data-ttu-id="48491-163">A primeira etapa é obter um índice TLS usando **TlsAlloc**, que deve ser liberado usando **TlsFree**.</span><span class="sxs-lookup"><span data-stu-id="48491-163">The first step is to obtain a TLS index by using **TlsAlloc**, which must ultimately be released using **TlsFree**.</span></span> <span data-ttu-id="48491-164">Ambos são mais bem realizados a partir de **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="48491-164">Both are best accomplished from **DllMain**.</span></span>
  
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

<span data-ttu-id="48491-165">Depois de obter o índice, a próxima etapa é alocar um bloco de memória para cada thread.</span><span class="sxs-lookup"><span data-stu-id="48491-165">After you obtain the index, the next step is to allocate a block of memory for each thread.</span></span> <span data-ttu-id="48491-166">A [Documentação de desenvolvimento do Windows](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) recomenda fazer isso toda vez que a função de retorno de chamada **DllMain** for chamada com um evento **DLL_THREAD_ATTACH** e liberando a memória em cada **DLL_THREAD_DETACH**.</span><span class="sxs-lookup"><span data-stu-id="48491-166">The [Windows Development Documentation](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) recommends doing this every time the **DllMain** callback function is called with a **DLL_THREAD_ATTACH** event, and freeing the memory on every **DLL_THREAD_DETACH**.</span></span> <span data-ttu-id="48491-167">No entanto, seguir esse aviso faria com que a sua DLL fizesse um trabalho desnecessário para threads não usados para recálculo.</span><span class="sxs-lookup"><span data-stu-id="48491-167">However, following this advice would cause your DLL to do unnecessary work for threads not used for recalculation.</span></span> 
  
<span data-ttu-id="48491-168">Em vez disso, é melhor usar uma estratégia de alocação no primeiro uso.</span><span class="sxs-lookup"><span data-stu-id="48491-168">Instead, it is better to use an allocate-on-first-use strategy.</span></span> <span data-ttu-id="48491-169">Primeiro, você precisa definir uma estrutura que queira alocar para cada thread.</span><span class="sxs-lookup"><span data-stu-id="48491-169">First, you need to define a structure that you want to allocate for each thread.</span></span> <span data-ttu-id="48491-170">Para os exemplos anteriores que retornam **XLOPERs** ou **XLOPER12s**, o seguinte é suficiente, mas você pode criar qualquer estrutura que atenda às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="48491-170">For the previous examples that return **XLOPERs** or **XLOPER12s**, the following suffices, but you can create any structure that satisfies your needs.</span></span>
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

<span data-ttu-id="48491-171">A função a seguir obtém um ponteiro para a instância local de thread ou aloca um caso essa seja a primeira chamada.</span><span class="sxs-lookup"><span data-stu-id="48491-171">The following function gets a pointer to the thread-local instance, or allocates one if this is the first call.</span></span>
  
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

<span data-ttu-id="48491-172">Agora, você pode ver como a memória **XLOPER/XLOPER12** local de thread é obtida: primeiro, você obtém um ponteiro para a instância de **TLS_data** do thread e, em seguida, retorna um ponteiro para o **XLOPER/XLOPER12** contido nele, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="48491-172">Now you can see how the thread-local **XLOPER/XLOPER12** memory is obtained: first, you get a pointer to the thread's instance of **TLS_data**, and then you return a pointer to the **XLOPER/XLOPER12** contained within it, as follows.</span></span> 
  
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

<span data-ttu-id="48491-173">As funções **mtr_safe_example_1** e **mtr_safe_example_2** podem ser registradas como funções de planilha thread-safe quando você está executando o Excel.</span><span class="sxs-lookup"><span data-stu-id="48491-173">The **mtr_safe_example_1** and **mtr_safe_example_2** functions can be registered as thread-safe worksheet functions when you are running Excel.</span></span> <span data-ttu-id="48491-174">No entanto, não é possível combinar as duas abordagens em um único XLL.</span><span class="sxs-lookup"><span data-stu-id="48491-174">However, you cannot mix the two approaches in one XLL.</span></span> <span data-ttu-id="48491-175">Seu XLL só pode exportar uma implementação de **xlAutoFree** e **xlAutoFree12**, e cada estratégia de memória requer uma abordagem diferente.</span><span class="sxs-lookup"><span data-stu-id="48491-175">Your XLL can only export one implementation of **xlAutoFree** and **xlAutoFree12**, and each memory strategy requires a different approach.</span></span> <span data-ttu-id="48491-176">Com **mtr_safe_example_1**, o ponteiro transmitido para **xlAutoFree/xlAutoFree12** deve ser liberado junto com quaisquer dados para os quais ele aponte.</span><span class="sxs-lookup"><span data-stu-id="48491-176">With **mtr_safe_example_1**, the pointer passed to **xlAutoFree/xlAutoFree12** must be freed along with any data it points to.</span></span> <span data-ttu-id="48491-177">Com **mtr_safe_example_2**, somente os dados apontados devem ser liberados.</span><span class="sxs-lookup"><span data-stu-id="48491-177">With **mtr_safe_example_2**, only the pointed-to data should be freed.</span></span>
  
<span data-ttu-id="48491-178">O Windows também fornece uma função **GetCurrentThreadId**, que retorna o ID exclusivo no âmbito do sistema do thread atual.</span><span class="sxs-lookup"><span data-stu-id="48491-178">Windows also provides a function **GetCurrentThreadId**, which returns the current thread's unique system-wide ID.</span></span> <span data-ttu-id="48491-179">Isso fornece ao desenvolvedor outra maneira de tornar o código thread-safe ou de tornar seu comportamento específico para o thread.</span><span class="sxs-lookup"><span data-stu-id="48491-179">This provides the developer with another way to make code thread safe, or to make its behavior thread specific.</span></span>
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a><span data-ttu-id="48491-180">Memória acessível somente por mais de um thread: seções críticas</span><span class="sxs-lookup"><span data-stu-id="48491-180">Memory Accessible Only by More than One Thread: Critical Sections</span></span>

<span data-ttu-id="48491-181">Você deve proteger a memória de leitura/gravação que pode ser acessada por mais de um thread usando seções críticas.</span><span class="sxs-lookup"><span data-stu-id="48491-181">You should protect read/write memory that can be accessed by more than one thread using critical sections.</span></span> <span data-ttu-id="48491-182">É necessário ter uma seção crítica nomeada para cada bloco de memória que você deseja proteger.</span><span class="sxs-lookup"><span data-stu-id="48491-182">You need a named critical section for each block of memory you want to protect.</span></span> <span data-ttu-id="48491-183">Essas seções podem ser inicializadas durante a chamada para a função **xlAutoOpen** e liberadas e definidas como nulas durante a chamada para a função **xlAutoClose**.</span><span class="sxs-lookup"><span data-stu-id="48491-183">You can initialize these during the call to the **xlAutoOpen** function, and release them and set them to null during the call to the **xlAutoClose** function.</span></span> <span data-ttu-id="48491-184">Em seguida, você precisa conter cada acesso ao bloco protegido em um par de chamadas para **EnterCriticalSection** e **LeaveCriticalSection**.</span><span class="sxs-lookup"><span data-stu-id="48491-184">You then need to contain each access to the protected block within a pair of calls to **EnterCriticalSection** and **LeaveCriticalSection**.</span></span> <span data-ttu-id="48491-185">Apenas um thread é permitido na seção crítica a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="48491-185">Only one thread is permitted into the critical section at any time.</span></span> <span data-ttu-id="48491-186">Veja a seguir um exemplo de inicialização, cancelamento da inicialização e uso de uma seção chamada **g_csSharedTable**.</span><span class="sxs-lookup"><span data-stu-id="48491-186">Here is an example of the initialization, uninitialization, and use of a section called **g_csSharedTable**.</span></span>
  
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

<span data-ttu-id="48491-187">Outra maneira, talvez mais segura, de proteger um bloco de memória é criar uma classe que contenha sua própria **CRITICAL_SECTION** e cujos métodos de construtor, destruidor e acessador cuidem do seu uso.</span><span class="sxs-lookup"><span data-stu-id="48491-187">Another, perhaps safer way of protecting a block of memory is to create a class that contains its own **CRITICAL_SECTION** and whose constructor, destructor, and accessor methods take care of its use.</span></span> <span data-ttu-id="48491-188">Essa abordagem tem a vantagem adicional de proteger objetos que possam ser inicializados antes da execução de **xlAutoOpen** ou que possam sobreviver após a chamada de **xlAutoClose**. Porém, você deve ter cuidado ao criar muitas seções críticas e com a sobrecarga que isso criaria no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="48491-188">This approach has the added advantage of protecting objects that may be initialized before **xlAutoOpen** is run, or survive after **xlAutoClose** is called, but you should be careful about creating too many critical sections and the operating system overhead that this would create.</span></span> 
  
<span data-ttu-id="48491-189">Quando existe um código que requer acesso a mais de um bloco de memória protegida ao mesmo tempo, é necessário considerar com muito cuidado a ordem de entrada e saída dessas seções críticas.</span><span class="sxs-lookup"><span data-stu-id="48491-189">When you have code that needs access to more than one block of protected memory at the same time, you need to consider very carefully the order in which the critical sections are entered and exited.</span></span> <span data-ttu-id="48491-190">Por exemplo, as duas funções a seguir podem criar um deadlock.</span><span class="sxs-lookup"><span data-stu-id="48491-190">For example, the following two functions could create a deadlock.</span></span>
  
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

<span data-ttu-id="48491-191">Se a primeira função em um thread inserir **g_csSharedTableA** enquanto a segunda em outro thread inserir **g_csSharedTableB**, ambos os segmentos travarão.</span><span class="sxs-lookup"><span data-stu-id="48491-191">If the first function on one thread enters **g_csSharedTableA** while the second on another thread enters **g_csSharedTableB**, both threads hang.</span></span> <span data-ttu-id="48491-192">A abordagem correta é entrar em uma ordem consistente e sair na ordem inversa, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="48491-192">The correct approach is to enter in a consistent order and exit in the reverse order, as follows.</span></span>
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

<span data-ttu-id="48491-193">Sempre que possível, sob o ponto de vista da cooperação de threads, é melhor isolar o acesso a blocos distintos, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="48491-193">Where possible, it is better from a thread co-operation point of view to isolate access to distinct blocks, as shown here.</span></span>
  
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

<span data-ttu-id="48491-194">Onde houver muita contenção por um recurso compartilhado, como solicitações frequentes de acesso de curta duração, considere usar a capacidade de rodízio da seção crítica.</span><span class="sxs-lookup"><span data-stu-id="48491-194">Where there is a lot of contention for a shared resource, such as frequent short-duration access requests, you should consider using the critical section's ability to spin.</span></span> <span data-ttu-id="48491-195">Essa é uma técnica que faz com que a espera pelo recurso exija o uso de menos recursos do processador.</span><span class="sxs-lookup"><span data-stu-id="48491-195">This is a technique that makes waiting for the resource less processor-intensive.</span></span> <span data-ttu-id="48491-196">Para fazer isso, você pode usar **InitializeCriticalSectionAndSpinCount** ao inicializar a seção ou **SetCriticalSectionSpinCount** uma vez que esta for inicializada, para definir o número de vezes que o thread executa um loop antes de aguardar a disponibilização de recursos.</span><span class="sxs-lookup"><span data-stu-id="48491-196">To do this, you can use either **InitializeCriticalSectionAndSpinCount** when initializing the section or **SetCriticalSectionSpinCount** once initialized, to set the number of times the thread loops before waiting for resources to become available.</span></span> <span data-ttu-id="48491-197">A operação de espera é dispendiosa e, portanto, o rodízio evita isso quando o recurso é liberado nesse meio tempo.</span><span class="sxs-lookup"><span data-stu-id="48491-197">The wait operation is expensive, so spinning avoids this if the resource is freed in the meantime.</span></span> <span data-ttu-id="48491-198">Em um sistema de processador único, a contagem de rodízio é efetivamente ignorada, mas você ainda pode especificá-la sem causar nenhum dano.</span><span class="sxs-lookup"><span data-stu-id="48491-198">On a single processor system, the spin count is effectively ignored, but you can still specify it without doing any harm.</span></span> <span data-ttu-id="48491-199">O gerenciador de heap de memória usa uma contagem de rodízio de 4000.</span><span class="sxs-lookup"><span data-stu-id="48491-199">The memory heap manager uses a spin count of 4000.</span></span> <span data-ttu-id="48491-200">Para obter mais informações sobre o uso de seções críticas, consulte a documentação do Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="48491-200">For more information about the use of critical sections, see the Windows SDK documentation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48491-201">Confira também</span><span class="sxs-lookup"><span data-stu-id="48491-201">See also</span></span>



[<span data-ttu-id="48491-202">Gerenciamento de Memória no Excel</span><span class="sxs-lookup"><span data-stu-id="48491-202">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="48491-203">Recálculo com vários threads no Excel</span><span class="sxs-lookup"><span data-stu-id="48491-203">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="48491-204">Gerenciador de Suplemento e Funções da Interface XLL</span><span class="sxs-lookup"><span data-stu-id="48491-204">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

