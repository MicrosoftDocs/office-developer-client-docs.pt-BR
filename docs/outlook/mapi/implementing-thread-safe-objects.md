---
title: Implementar objetos livres de threads
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2f8235caceec8b27b2b14fac26d51e9e31ce1024
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579771"
---
# <a name="implementing-thread-safe-objects"></a>Implementar objetos livres de threads

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Com os objetos que são retornados de chamadas de métodos de interface diretamente, é responsabilidade do provedor para garantir a segurança do thread. Com objetos de retorno de chamada, é responsabilidade do aplicativo cliente.
  
Um cliente pode implementar um retorno de chamada de notificação de thread-safe chamando-se o utilitário MAPI [HrThisThreadAdviseSink](hrthisthreadadvisesink.md). **HrThisThreadAdviseSink** transforma um coletor de não-thread-safe advise em um thread-safe. Para retornos de chamada de progresso, não há nenhuma dessas utilitário. Um cliente pode optar por usar o objeto de progresso de thread-safe MAPI ou criá-lo manualmente. 
  
Um objeto de thread-safe pode ou não também pode estar ciente de segmento. Um objeto de reconhecimento de threads mantém um contexto separado para cada segmento que está sendo usada. Provedores de serviços não são necessário para suportar o reconhecimento de thread em seus objetos thread-safe, embora o suporte ao reconhecimento de thread pode ser útil em algumas situações. Duas tabelas MAPI sempre fornecem seu próprio contexto por definição. Uma única tabela usada em threads diferentes não e não deve fornecer o contexto exclusivo.
  
Um cliente pode escolher entre receber notificações na mesma thread que foi usado para o **MAPIInitialize** chamar, no mesmo thread que foi usado para a chamada **Advise** ou em um segmento separado pertencentes a MAPI. Para garantir que as notificações cheguem no mesmo thread que foi usado para chamar **MAPIInitialize**, um cliente chama [MAPIInitialize](mapiinitialize.md) e passa zero no membro **ulFlags** da estrutura [MAPIINIT_0](mapiinit_0.md) . Notificações, em seguida, são entregues durante o loop de mensagem principal. 
  
Para receber notificações no thread de propriedade MAPI, um cliente chama **MAPIInitialize** com o membro **ulFlags** da estrutura **MAPIINIT_0** definida como MAPI_MULTITHREAD_NOTIFICATIONS. A chamada de **Advise** é feita com o cliente avise o objeto coletor de eventos em vez de uma versão com quebra. 
  
Para garantir que as notificações cheguem no mesmo thread que foi usado para chamar **Advise**, um cliente chama [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) e passa que o recém-criado quebrado coletor de eventos para **Advise** , e não o coletor de eventos advise original de aviso. **MAPIInitialize** pode ser chamado com qualquer valor de sinalizador. 
  

