---
title: Implementando Thread-Safe objetos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9160136542c7960bad0be2423872171b17d99fe3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413525"
---
# <a name="implementing-thread-safe-objects"></a>Implementando Thread-Safe objetos

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Com objetos que são retornados de chamadas de método de interface diretamente, é responsabilidade do provedor garantir a segurança do thread. Com objetos de retorno de chamada, é responsabilidade do aplicativo cliente.
  
Um cliente pode implementar um retorno de chamada de notificação thread-safe chamando o utilitário DE MAPI [HrThisThreadAdviseSink](hrthisthreadadvisesink.md). **HrThisThreadAdviseSink** transforma um sink não seguro para threads em um thread-safe. Para retornos de chamada de progresso, esse utilitário não existe. Um cliente pode optar por usar o objeto de progresso seguro para threads MAPI ou criar um manualmente. 
  
Um objeto thread-safe também pode ou não estar ciente do thread. Um objeto que reconhece threads mantém um contexto separado para cada thread que o está usando. Os provedores de serviços não são necessários para oferecer suporte ao reconhecimento de threads em seus objetos thread-safe, embora o suporte ao reconhecimento de threads possa ser útil em algumas situações. Duas tabelas MAPI sempre fornecem seu próprio contexto por definição. Uma tabela usada em threads diferentes não fornece e não deve fornecer contexto exclusivo.
  
Um cliente pode escolher entre receber notificações no mesmo thread que foi usado para a chamada **MAPIInitialize,** no mesmo thread que foi usado para a chamada De aviso ou em um thread separado pertencente a MAPI.  Para garantir que as notificações cheguem no mesmo thread que foi usado para chamar **MAPIInitialize**, um cliente chama [MAPIInitialize](mapiinitialize.md) e passa zero no **membro ulFlags** da estrutura [MAPIINIT_0.](mapiinit_0.md) As notificações são então entregues durante o loop da mensagem principal. 
  
Para receber notificações no thread de propriedade de MAPI, um cliente chama **MAPIInitialize** com o membro **ulFlags** da estrutura **MAPIINIT_0** definida como MAPI_MULTITHREAD_NOTIFICATIONS. A **chamada Advise** é feita com o objeto de pia de conselhos do cliente em vez de uma versão empacotada. 
  
Para garantir que as notificações cheguem no mesmo thread que foi usado para chamar **Advise**, um cliente chama [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) e passa o cliente recém-criado empacotado para **Aviso,** em vez do pia de aviso original. **MAPIInitialize** pode ser chamado com qualquer valor de sinalizador. 
  

