---
title: Chamar MAPI de serviços do Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318100"
---
# <a name="calling-mapi-from-windows-services"></a>Chamar MAPI de serviços do Windows

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para permitir que os aplicativos cliente MAPI escritos como serviços do Windows operem com provedores de serviço compatíveis com MAPI, o MAPI impõe diversas limitações e requisitos.
  
Os clientes MAPI têm as seguintes limitações:
  
- Eles não podem permitir uma interface de usuário.
    
- Eles podem enviar mensagens apenas por meio de um repositório de mensagens rigidamente acoplado e um provedor de transporte. Além disso, os clientes MAPI podem enviar e receber mensagens usando apenas o Microsoft Exchange Server ou outro provedor de transporte baseado em servidor. Devido a problemas de segurança e identidade entre aplicativos cliente e o spooler MAPI, a maioria dos provedores de transporte não é suportada em um serviço. 
    
Todos os aplicativos clientes MAPI, se são implementados como serviços do Windows, devem chamar a função [MAPIInitialize](mapiinitialize.md) para inicializar as bibliotecas MAPI. Uma chamada para a função [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) também é necessária para usar as bibliotecas OLE. Tanto [MAPIInitialize](mapiinitialize.md) quanto [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) fazem chamadas para a [](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) função CoInitialize para inicializar as bibliotecas de Component Object Model (com). Os clientes que são serviços devem definir um sinalizador especial, MAPI_NT_SERVICE, no membro **parâmetroulflags** da estrutura [MAPIINIT_0](mapiinit_0.md) que é passado para [MAPIInitialize](mapiinitialize.md) e no parâmetro _parâmetroulflags_ que é passado para o [funçãomapilogonex](mapilogonex.md) função para informar o MAPI de sua implementação especial. 
  
Os clientes MAPI escritos como serviços do Windows e escritos com a interface de cliente MAPI têm um requisito adicional. Eles devem definir o sinalizador MAPI_NO_MAIL na chamada para [funçãomapilogonex](mapilogonex.md). Outros tipos de clientes não precisam definir um sinalizador para logon porque ele é automaticamente definido por MAPI.
  
Para lidar com mensagens em um thread de inicialização, um cliente MAPI que é implementado como um serviço faz o seguinte:
  
1. Chama a função [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) quando o thread principal é bloqueado. 
    
2. Chama a sequência [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)e [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) das funções do Windows para manipular a mensagem quando [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) retorna a soma do valor do parâmetro _nCount_ e o valor de **WAIT_OBJECT_0**, que indica que uma mensagem está na fila.
    
## <a name="see-also"></a>Confira também



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Problemas do ambiente operacional](operating-environment-issues.md)

