---
title: Finalizar uma sessão MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 74c2a7247df02570761247a9e4a6fae378f37312
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385194"
---
# <a name="ending-a-mapi-session"></a>Finalizar uma sessão MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes podem terminar suas sessões em resposta a uma solicitação do usuário, seja imediatamente ou mensagens de saída depois que todos tiverem sido processadas e quando ocorre um erro crítico. Alguns clientes precisam ficar conectado para que mensagens de saída pendentes pode alcançar o provedor de transporte e o sistema de mensagens de destino. Se tais um cliente envia uma mensagem e imediatamente fizer logoff, a mensagem pode permanecer na fila de saída até que um usuário fizer logon novamente e permanece conectado tempo suficiente para que a mensagem a ser transmitida.
  
 **Quando você precisar encerrar a sessão com o subsistema MAPI**
  
1. Cancele os registros para todas as notificações chamando o método **Unadvise** de todos os objetos registrados. 
    
2. Libere todos os objetos abertos chamando os métodos [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) . Os tipos de objetos open podem incluir PIAs, a tabela de status, pasta caixa de saída, um ou mais armazenamentos de mensagem e o catálogo de endereços de aviso. 
    
3. Chame [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória para qualquer identificadores de entrada de cache, como **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
4. Chame [IMAPISession::Logoff](imapisession-logoff.md), definindo o sinalizador MAPI_LOGOFF_UI se você permitir a interface do usuário e o sinalizador MAPI_LOGOFF_SHARED se você é proprietário da sessão compartilhada atual. **Fazer logoff** notifica todos os outros clientes que estão usando a atual sessão compartilhada que eles devem fazer logoff enviando uma notificação de erro. 
    
5. Libere o ponteiro de sessão chamando o método de **IUnknown:: Release** da sessão. 
    
6. Se você chamado [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) durante a inicialização de sessão para inicializar as bibliotecas OLE, não inicializá-los agora chamando [OleUninitialize](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx). Somente os clientes que têm chamado **OleInitialize** devem chamar **OleUninitialize**. 
    
7. Não inicializar as bibliotecas MAPI chamando [MAPIUninitialize](mapiuninitialize.md). Se você chamado **OleInitialize** em algum momento, certifique-se de que uma chamada para **OleUninitialize** ocorre antes essa chamada para **MAPIUninitialize**. O tempo é crucial. Se a chamada para **OleUninitialize** segue a chamada para **MAPIUninitialize**, seu cliente pode ser encerrada maneira brusca. 
    
8. Se você chamado [ScInitMapiUtil](scinitmapiutil.md) durante a inicialização de sessão para inicializar a biblioteca do utilitário MAPI, não inicializá-lo agora chamando [DeinitMapiUtil](deinitmapiutil.md). Somente os clientes que têm chamado **ScInitMapiUtil** devem chamar **DeinitMapiUtil**.
    
> [!NOTE]
> Todos os objetos abertos devem ser liberados antes da chamada para **IMAPISession::Logoff**. Os objetos que permanecem abertos depois **Logoff** é chamado se tornam inválidos; eles não podem aceitar qualquer chamadas e nunca podem ser liberados. Se for feita uma chamada para um desses objetos, esperar que a chamada falhe. 
  
 MAPI não tem nenhum mecanismo para excluir DLLs durante o processo de encerramento da sessão. Um serviço que só pode ser excluída quando um cliente de configuração, como o painel de controle chama seu função do ponto de entrada do serviço de mensagem com o evento MSG_SERVICE_INSTALL DLL do provedor. 
  

