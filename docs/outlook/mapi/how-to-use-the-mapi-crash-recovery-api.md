---
title: Usar a API de recuperação de falhas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 41d70c2ab94712e40de9011bc752c79d8c859161
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595178"
---
# <a name="use-the-mapi-crash-recovery-api"></a><span data-ttu-id="c0519-103">Usar a API de recuperação de falhas MAPI</span><span class="sxs-lookup"><span data-stu-id="c0519-103">Use the MAPI Crash Recovery API</span></span>

<span data-ttu-id="c0519-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0519-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0519-105">Este tópico contém um exemplo de código em C++ que mostra como chamar a função [MAPICrashRecovery](mapicrashrecovery.md) da função [UnhandledExceptionFilter](http://msdn.microsoft.com/en-us/library/ms681401%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c0519-105">This topic contains a code sample in C++ that shows how to call the [MAPICrashRecovery](mapicrashrecovery.md) function from the [UnhandledExceptionFilter](http://msdn.microsoft.com/en-us/library/ms681401%28VS.85%29.aspx) function.</span></span> <span data-ttu-id="c0519-106">A função de [MAPICrashRecovery](mapicrashrecovery.md) verifica que o estado do arquivo de pastas particulares (. PST) ou o arquivo de pastas Offline (OST) a memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="c0519-106">The [MAPICrashRecovery](mapicrashrecovery.md) function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> 

<span data-ttu-id="c0519-107">Se a memória estiver em um estado consistente, a função [MAPICrashRecovery](mapicrashrecovery.md) move os dados em disco e impede que o maior acesso de leitura ou gravação até que o processo é encerrado.</span><span class="sxs-lookup"><span data-stu-id="c0519-107">If the memory is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> <span data-ttu-id="c0519-108">Garantindo que o PSTs ou OSTs estão em um estado consistente antes do processo é encerrado, você pode impedir que o Microsoft Outlook 2010 ou o Microsoft Outlook 2013 exiba a seguinte mensagem de erro e evitar problemas de desempenho:</span><span class="sxs-lookup"><span data-stu-id="c0519-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2010 or Microsoft Outlook 2013 from displaying the following error message and avoid performance problems:</span></span> 
  
<span data-ttu-id="c0519-109">**Um arquivo de dados não foi fechado corretamente a última vez que foi usada e está sendo verificada para problemas. Desempenho poderá ser afetado enquanto a seleção estiver em andamento.**</span><span class="sxs-lookup"><span data-stu-id="c0519-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
```cpp
LONG WINAPI UnhandledExceptionFilter(__in EXCEPTION_POINTERS* pep) 
{ 
    // Let the OS terminate the process upon return. 
    LONG retval = EXCEPTION_EXECUTE_HANDLER; 
 
    switch (pep->ExceptionRecord->ExceptionCode) 
    { 
        case EXCEPTION_BREAKPOINT: 
        case EXCEPTION_SINGLE_STEP: 
            // Ignore debugging exceptions. 
            retval = EXCEPTION_CONTINUE_SEARCH; 
            break; 
 
        default: 
            // The process is going to be terminated, so disconnect the MAPI database. 
            MAPICrashRecovery(MAPICRASH_RECOVER); 
            // Optionally, you can display a crash reporting dialog box here. 
            // If the user chooses to debug,  
            // call MAPICrashRecovery(MAPICRASH_CONTINUE). 
            break; 
    } 
 
    return retval; 
}
```

## <a name="see-also"></a><span data-ttu-id="c0519-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0519-110">See also</span></span>

- [<span data-ttu-id="c0519-111">Sobre a API de recuperação de falhas MAPI</span><span class="sxs-lookup"><span data-stu-id="c0519-111">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md) 
- [<span data-ttu-id="c0519-112">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="c0519-112">MAPICrashRecovery</span></span>](mapicrashrecovery.md)

