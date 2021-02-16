---
title: Encerrando uma sessão MAPI
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
# <a name="ending-a-mapi-session"></a>Encerrando uma sessão MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes podem encerrar suas sessões em resposta à solicitação de um usuário, imediatamente ou depois que todas as mensagens de saída foram processadas e quando ocorre um erro crítico. Alguns clientes precisam permanecer conectados para que as mensagens de saída pendentes possam alcançar o provedor de transporte e o sistema de mensagens de destino. Se esse cliente enviar uma mensagem e efetuar logo off imediatamente, a mensagem poderá permanecer na fila de saída até que um usuário esvasse e permaneça conectado por tempo suficiente para que a mensagem seja transmitida.
  
 **Quando você precisar encerrar sua sessão com o subsistema MAPI**
  
1. Cancele os registros de todas as notificações chamando o **método Unadvise** de cada objeto registrado. 
    
2. Libere todos os objetos abertos chamando seus [métodos IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) Os tipos de objetos abertos podem incluir aconselhá-los, a tabela de status, a pasta Caixa de Saída, um ou mais armazenamentos de mensagens e o livro de endereços. 
    
3. Chame [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória para quaisquer identificadores de entrada em cache, como **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
4. Chame [IMAPISession::Logoff](imapisession-logoff.md), definindo o sinalizador MAPI_LOGOFF_UI se você permitir uma interface do usuário e o sinalizador MAPI_LOGOFF_SHARED se for o próprio da sessão compartilhada atual. **Logoff** notifica todos os outros clientes que estão usando a sessão compartilhada atual que eles devem fazer logoff enviando uma notificação de erro. 
    
5. Libere o ponteiro da sessão chamando o método **IUnknown::Release da** sessão. 
    
6. Se você chamou [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) durante a inicialização da sessão para inicializar as bibliotecas OLE, não inicialize-as agora chamando [OleUninitialize](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx). Somente clientes que tenham chamado **OleInitialize** devem chamar **OleUninitialize**. 
    
7. Uninitialize as bibliotecas MAPI chamando [MAPIUninitialize](mapiuninitialize.md). Se você chamou **OleInitialize** em algum momento, certifique-se de que uma chamada para **OleUninitialize** ocorra antes dessa chamada para **MAPIUninitialize**. O tempo é crucial. Se a chamada para **OleUninitialize** seguir a chamada para **MAPIUninitialize**, seu cliente poderá ser encerrado de forma ingrato. 
    
8. Se você chamou [ScInitMapiUtil](scinitmapiutil.md) durante a inicialização da sessão para inicializar a biblioteca de utilitários MAPI, desincialize-a agora chamando [DeinitMapiUtil](deinitmapiutil.md). Somente clientes que tenham chamado **ScInitMapiUtil devem** chamar **DeinitMapiUtil**.
    
> [!NOTE]
> Todos os objetos abertos devem ser liberados antes da chamada para **IMAPISession::Logoff**. Os objetos que permanecem abertos depois **que Logoff** é chamado tornam-se inválidos; eles não podem aceitar chamadas e podem nunca ser liberados. Se uma chamada for feita para um desses objetos, espere que a chamada falhe. 
  
 O MAPI não tem mecanismo para excluir DLLs durante o processo de desligamento da sessão. A DLL de um provedor de serviços só pode ser excluída quando um cliente de configuração como o Painel de Controle chama sua função de ponto de entrada do serviço de mensagens com o MSG_SERVICE_INSTALL evento. 
  

