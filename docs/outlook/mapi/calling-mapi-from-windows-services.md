---
title: Chamando MAPI de Serviços do Windows
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
# <a name="calling-mapi-from-windows-services"></a>Chamando MAPI de Serviços do Windows

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para permitir que aplicativos cliente MAPI gravados como serviços do Windows operem com provedores de serviços compatíveis com MAPI, o MAPI impõe várias limitações e requisitos.
  
Os clientes MAPI têm as seguintes limitações:
  
- Eles não podem permitir uma interface do usuário.
    
- Eles só podem enviar mensagens por meio de um provedor de transporte e armazenamento de mensagens fortemente a par. Além disso, os clientes MAPI podem enviar e receber mensagens usando apenas o Microsoft Exchange Server ou outro provedor de transporte baseado em servidor. Devido a problemas de identidade e segurança entre aplicativos cliente e o spooler MAPI, a maioria dos provedores de transporte não é suportada em um serviço. 
    
Todos os aplicativos cliente MAPI, sejam eles implementados como serviços do Windows, devem chamar a função [MAPIInitialize](mapiinitialize.md) para inicializar as bibliotecas MAPI. Uma chamada para a [função OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) também é necessária para usar as bibliotecas OLE. [MAPIInitialize](mapiinitialize.md) e [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) fazem chamadas para a função [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) para inicializar as bibliotecas com (Component Object Model). Os clientes que são serviços devem definir um sinalizador especial, MAPI_NT_SERVICE, no **membro ulFlags** da estrutura MAPIINIT_0 que é passada para [MAPIInitialize](mapiinitialize.md) e no _parâmetro ulFlags_ que é passado para [a](mapiinit_0.md) função [MAPILogonEx](mapilogonex.md) para informar o MAPI de sua implementação especial. 
  
Clientes MAPI escritos como serviços do Windows e escritos com a interface do cliente MAPI têm um requisito adicional. Eles devem definir o MAPI_NO_MAIL sinalizador na chamada para [MAPILogonEx](mapilogonex.md). Outros tipos de clientes não têm que definir um sinalizador para logon porque ele é definido automaticamente pelo MAPI.
  
Para manipular mensagens em um thread de inicialização, um cliente MAPI implementado como um serviço faz o seguinte:
  
1. Chama a [função MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) quando o thread principal é bloco. 
    
2. Chama a sequência [getMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)e [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) de funções do Windows para manipular a mensagem quando [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) retorna a soma do valor do parâmetro  _nCount_ e o valor de **WAIT_OBJECT_0**, que indica que uma mensagem está na fila.
    
## <a name="see-also"></a>Confira também



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Problemas do ambiente operacional](operating-environment-issues.md)

