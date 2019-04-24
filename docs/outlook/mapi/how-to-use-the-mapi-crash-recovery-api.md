---
title: Usar a API de recuperação de falhas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: a73889982e4aa72fb664a8eafd6fc8704e581e98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346421"
---
# <a name="use-the-mapi-crash-recovery-api"></a><span data-ttu-id="f94c4-103">Usar a API de recuperação de falhas MAPI</span><span class="sxs-lookup"><span data-stu-id="f94c4-103">Use the MAPI Crash Recovery API</span></span>

<span data-ttu-id="f94c4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f94c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f94c4-105">Este tópico contém um exemplo de código em C++ que mostra como chamar a função [MAPICrashRecovery](mapicrashrecovery.md) da função [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f94c4-105">This topic contains a code sample in C++ that shows how to call the [MAPICrashRecovery](mapicrashrecovery.md) function from the [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) function.</span></span> <span data-ttu-id="f94c4-106">A função [MAPICrashRecovery](mapicrashrecovery.md) verifica o estado do arquivo de pastas particulares (PST) ou da memória compartilhada do arquivo de pastas offline (OST).</span><span class="sxs-lookup"><span data-stu-id="f94c4-106">The [MAPICrashRecovery](mapicrashrecovery.md) function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> 

<span data-ttu-id="f94c4-107">Se a memória estiver em um estado consistente, a função [MAPICrashRecovery](mapicrashrecovery.md) moverá os dados para o disco e impedirá o acesso de leitura ou gravação adicional até que o processo seja encerrado.</span><span class="sxs-lookup"><span data-stu-id="f94c4-107">If the memory is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> <span data-ttu-id="f94c4-108">Ao garantir que PSTs ou OSTs estejam em um estado consistente antes do término do processo, você pode impedir que o Microsoft Outlook 2010 ou o Microsoft Outlook 2013 exiba a mensagem de erro a seguir e evitar problemas de desempenho:</span><span class="sxs-lookup"><span data-stu-id="f94c4-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2010 or Microsoft Outlook 2013 from displaying the following error message and avoid performance problems:</span></span> 
  
<span data-ttu-id="f94c4-109">**Um arquivo de dados não foi fechado corretamente na última vez em que foi usado e está sendo verificado em busca de problemas. O desempenho pode ser afetado enquanto o cheque estiver em andamento.**</span><span class="sxs-lookup"><span data-stu-id="f94c4-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="f94c4-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="f94c4-110">See also</span></span>

- [<span data-ttu-id="f94c4-111">Sobre a API de recuperação de falhas MAPI</span><span class="sxs-lookup"><span data-stu-id="f94c4-111">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md) 
- [<span data-ttu-id="f94c4-112">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="f94c4-112">MAPICrashRecovery</span></span>](mapicrashrecovery.md)

