---
title: Implementar objetos isentos de threads
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
# <a name="implementing-thread-safe-objects"></a>Implementar objetos isentos de threads

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Com objetos que são retornados de chamadas de método de interface diretamente, é responsabilidade do provedor garantir a segurança do thread. Com objetos de retorno de chamada, é responsabilidade do aplicativo cliente.
  
Um cliente pode implementar um retorno de chamada de notificação thread-safe chamando o utilitário MAPI [HrThisThreadAdviseSink](hrthisthreadadvisesink.md). O **HrThisThreadAdviseSink** transforma um coletor de aviso não isento de threads em um thread seguro. Para retornos de chamada de progresso, não há esse utilitário. Um cliente pode optar por usar o objeto de progresso thread-safe de MAPI ou criar um manualmente. 
  
Um objeto thread-safe pode ou não ser compatível com threads. Um objeto com reconhecimento de thread mantém um contexto separado para cada thread que o está usando. Os provedores de serviços não são necessários para dar suporte ao reconhecimento de threads em seus objetos isentos de threads, embora o suporte a reconhecimento de threads possa ser útil em algumas situações. Duas tabelas MAPI sempre fornecem seu próprio contexto por definição. Uma tabela usada em threads diferentes não e deve fornecer contexto exclusivo.
  
Um cliente pode escolher entre receber notificações no mesmo thread que foi usado para a chamada **MAPIInitialize** , no mesmo thread que foi usado para a chamada de **aviso** ou em um thread separado de Propriedade do MAPI. Para garantir que as notificações cheguem no mesmo thread que foi usado para chamar **MAPIInitialize**, um cliente chama o [MAPIInitialize](mapiinitialize.md) e passa zero no membro **parâmetroulflags** da estrutura [MAPIINIT_0](mapiinit_0.md) . As notificações são entregues durante o loop de mensagem principal. 
  
Para receber notificações no thread de propriedade de MAPI, um cliente chama **MAPIInitialize** com o membro **Parâmetroulflags** da estrutura **MAPIINIT_0** definida como MAPI_MULTITHREAD_NOTIFICATIONS. A chamada de **aviso** é feita com o objeto de coletor de aviso do cliente em vez de uma versão encapsulada. 
  
Para garantir que as notificações sejam recebidas no mesmo thread que foi usado para chamar o **aviso**, um cliente chama [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) e passa o coletor de aviso com invólucro recém-criado para **aconselhar** em vez do coletor de aviso original. **MAPIInitialize** pode ser chamado com um valor de sinalizador. 
  

