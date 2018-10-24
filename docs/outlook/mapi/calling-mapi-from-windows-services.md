---
title: Chamar o MAPI a partir dos Serviços do Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385575"
---
# <a name="calling-mapi-from-windows-services"></a>Chamar o MAPI a partir dos Serviços do Windows

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para permitir que aplicativos de cliente MAPI que são gravados como serviços do Windows para operar com provedores de serviço compatível com MAPI, MAPI impõe vários requisitos e limitações.
  
Clientes MAPI têm as seguintes limitações:
  
- Eles não podem permitir uma interface do usuário.
    
- Eles podem enviar mensagens apenas por meio de um repositório de ligação estreita de mensagem e transporte de provedor. Além disso, os clientes MAPI podem enviar e receber mensagens usando apenas o Microsoft Exchange Server ou outro provedor de transporte baseado em servidor. Devido a problemas de segurança e de identidade entre aplicativos cliente e o spooler MAPI, a maioria dos provedores de transporte não são suportados em um serviço. 
    
Todos os aplicativos de cliente MAPI, se eles são implementados como serviços do Windows, devem chamar a função [MAPIInitialize](mapiinitialize.md) para inicializar as bibliotecas MAPI. Uma chamada para a função [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) também é necessária usar as bibliotecas OLE. [MAPIInitialize](mapiinitialize.md) e o [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) fazem chamadas para a função [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) para inicializar as bibliotecas de modelo COM (Component Object). Clientes que são serviços devem definir um sinalizador especial, MAPI_NT_SERVICE, no membro **ulFlags** da estrutura [MAPIINIT_0](mapiinit_0.md) que é passado para [MAPIInitialize](mapiinitialize.md) e no parâmetro _ulFlags_ que é passado para o [MAPILogonEx](mapilogonex.md) função para informar MAPI de sua implementação especial. 
  
Clientes MAPI que são gravados como serviços do Windows e gravados com a interface de cliente MAPI tem um requisito adicional. Eles devem definir o sinalizador MAPI_NO_MAIL na chamada a [MAPILogonEx](mapilogonex.md). Outros tipos de clientes não precisará definir um sinalizador para logon porque ela é definida automaticamente pelo MAPI.
  
Para processar mensagens em um segmento de inicialização, um cliente MAPI que é implementado como um serviço faz o seguinte:
  
1. Chama a função [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) quando os blocos de thread principal. 
    
2. Chama a sequência [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx) [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)e [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) das funções do Windows para lidar com a mensagem quando [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) retorna a soma do valor do parâmetro _nCount_ e o valor de **WAIT_OBJECT_0**, que indica que uma mensagem está na fila.
    
## <a name="see-also"></a>Confira também



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Problemas operacionais no ambiente](operating-environment-issues.md)

