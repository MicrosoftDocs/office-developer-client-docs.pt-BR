---
title: Chamar o MAPI a partir dos Serviços do Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f77b3dd9ca8c977574aab337b0df572404061b4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565862"
---
# <a name="calling-mapi-from-windows-services"></a>Chamar o MAPI a partir dos Serviços do Windows

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para permitir que aplicativos de cliente MAPI que são gravados como serviços do Windows para operar com provedores de serviço compatível com MAPI, MAPI impõe vários requisitos e limitações.
  
Clientes MAPI têm as seguintes limitações:
  
- Eles não podem permitir uma interface do usuário.
    
- Eles podem enviar mensagens apenas por meio de um repositório de ligação estreita de mensagem e transporte de provedor. Além disso, os clientes MAPI podem enviar e receber mensagens usando apenas o Microsoft Exchange Server ou outro provedor de transporte baseado em servidor. Devido a problemas de segurança e de identidade entre aplicativos cliente e o spooler MAPI, a maioria dos provedores de transporte não são suportados em um serviço. 
    
Todos os aplicativos de cliente MAPI, se eles são implementados como serviços do Windows, devem chamar a função [MAPIInitialize](mapiinitialize.md) para inicializar as bibliotecas MAPI. Uma chamada para a função [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) também é necessária usar as bibliotecas OLE. [MAPIInitialize](mapiinitialize.md) e o [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) fazem chamadas para a função [CoInitialize](http://msdn.microsoft.com/en-us/library/ms678543%28VS.85%29.aspx) para inicializar as bibliotecas de modelo COM (Component Object). Clientes que são serviços devem definir um sinalizador especial, MAPI_NT_SERVICE, no membro **ulFlags** da estrutura [MAPIINIT_0](mapiinit_0.md) que é passado para [MAPIInitialize](mapiinitialize.md) e no parâmetro _ulFlags_ que é passado para o [MAPILogonEx](mapilogonex.md) função para informar MAPI de sua implementação especial. 
  
Clientes MAPI que são gravados como serviços do Windows e gravados com a interface de cliente MAPI tem um requisito adicional. Eles devem definir o sinalizador MAPI_NO_MAIL na chamada a [MAPILogonEx](mapilogonex.md). Outros tipos de clientes não precisará definir um sinalizador para logon porque ela é definida automaticamente pelo MAPI.
  
Para processar mensagens em um segmento de inicialização, um cliente MAPI que é implementado como um serviço faz o seguinte:
  
1. Chama a função [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) quando os blocos de thread principal. 
    
2. Chama a sequência [GetMessage](http://msdn.microsoft.com/en-us/library/ms644936%28VS.85%29.aspx) [TranslateMessage](http://msdn.microsoft.com/en-us/library/ms644955%28VS.85%29.aspx)e [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934%28VS.85%29.aspx) das funções do Windows para lidar com a mensagem quando [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) retorna a soma do valor do parâmetro _nCount_ e o valor de **WAIT_OBJECT_0**, que indica que uma mensagem está na fila.
    
## <a name="see-also"></a>Confira também



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Problemas do ambiente de operação](operating-environment-issues.md)

