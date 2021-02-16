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
# <a name="use-the-mapi-crash-recovery-api"></a>Usar a API de recuperação de falhas MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico contém um exemplo de código em C++ que mostra como chamar a função [MAPICrashRecovery](mapicrashrecovery.md) da [função UnhandledExceptionFilter.](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) A [função MAPICrashRecovery](mapicrashrecovery.md) verifica o estado da memória compartilhada do arquivo de Pastas Particulares (PST) ou do arquivo de Pastas Offline (OST). 

Se a memória estiver em um estado consistente, a função [MAPICrashRecovery](mapicrashrecovery.md) move os dados para o disco e impede acesso de leitura ou gravação até que o processo seja encerrado. Ao garantir que os PSTs ou OSTs estão em um estado consistente antes que o processo seja encerrado, você pode impedir que o Microsoft Outlook 2010 ou o Microsoft Outlook 2013 exibir a seguinte mensagem de erro e evitar problemas de desempenho: 
  
**Um arquivo de dados não foi fechado corretamente na última vez em que foi usado e está sendo verificado em busca de problemas. O desempenho pode ser afetado enquanto a verificação está em andamento.**
  
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

## <a name="see-also"></a>Confira também

- [Sobre a API de recuperação de falhas MAPI](about-the-mapi-crash-recovery-api.md) 
- [MAPICrashRecovery](mapicrashrecovery.md)

