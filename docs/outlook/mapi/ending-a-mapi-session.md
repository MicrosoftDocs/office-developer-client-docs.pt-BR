---
title: Finalizar uma sessão MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 74c2a7247df02570761247a9e4a6fae378f37312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287150"
---
# <a name="ending-a-mapi-session"></a>Finalizar uma sessão MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes podem encerrar suas sessões em resposta a uma solicitação do usuário, imediatamente ou após todas as mensagens de saída terem sido processadas e quando ocorre um erro crítico. Alguns clientes precisam permanecer conectados para que as mensagens de saída pendentes possam alcançar o provedor de transporte e o sistema de mensagens de destino. Se tal cliente enviar uma mensagem e efetuar logoff imediatamente, a mensagem poderá permanecer na fila de saída até que um usuário faça logon novamente e permaneça conectado o tempo suficiente para que a mensagem seja transmitida.
  
 **Quando você precisa encerrar a sessão com o subsistema MAPI**
  
1. Cancele os registros de todas as notificações chamando o método **Unadvise** de cada objeto registrado. 
    
2. Libere todos os objetos abertos chamando seus métodos [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) . Os tipos de objetos abertos podem incluir coletores de aviso, a tabela de status, a pasta de saída, um ou mais repositórios de mensagens e o catálogo de endereços. 
    
3. Chame [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória para qualquer identificador de entrada em cache, como **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
4. Chame [IMAPISession:: logoff](imapisession-logoff.md), definindo o sinalizador MAPI_LOGOFF_UI se você permitir uma interface de usuário e o sinalizador MAPI_LOGOFF_SHARED se você for proprietário da sessão compartilhada atual. O **logoff** notifica todos os outros clientes que estão usando a sessão compartilhada atual que eles devem fazer logoff enviando uma notificação de erro. 
    
5. Solte o ponteiro da sessão chamando o método **IUnknown:: Release** da sessão. 
    
6. Se você chamou [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) durante a inicialização da sessão para inicializar as bibliotecas OLE, desinicialize-as agora chamando [OleUninitialize](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx). Somente os clientes que chamaram **OleInitialize** devem chamar **OleUninitialize**. 
    
7. Desinicialize as bibliotecas MAPI chamando [MAPIUninitialize](mapiuninitialize.md). Se você chamou **OleInitialize** em algum momento, certifique-se de que uma chamada para **OleUninitialize** ocorre antes desta chamada para **MAPIUninitialize**. O tempo é crucial. Se a chamada para **OleUninitialize** seguir a chamada para **MAPIUninitialize**, seu cliente poderá terminar de forma não-normal. 
    
8. Se você chamou [ScInitMapiUtil](scinitmapiutil.md) durante a inicialização da sessão para inicializar a biblioteca de utilitários MAPI, desinicialize-o agora chamando [DeinitMapiUtil](deinitmapiutil.md). Somente os clientes que chamaram **ScInitMapiUtil** devem chamar **DeinitMapiUtil**.
    
> [!NOTE]
> Todos os objetos abertos devem ser liberados antes da chamada para **IMAPISession:: logoff**. Os objetos que permanecem abertos após o **logoff** é chamado se tornam inválidos; Eles não podem aceitar chamadas e nunca podem ser liberados. Se uma chamada for feita a um desses objetos, espere a chamada falhar. 
  
 O MAPI não tem nenhum mecanismo para excluir DLLs durante o processo de encerramento da sessão. Uma DLL do provedor de serviços só pode ser excluída quando um cliente de configuração, como o painel de controle, chama sua função de ponto de entrada de serviço de mensagens com o evento MSG_SERVICE_INSTALL. 
  

