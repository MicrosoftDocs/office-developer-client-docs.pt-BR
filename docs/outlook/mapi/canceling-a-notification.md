---
title: Cancelar uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 50d1fb451cbfcd07f97c5b12a9c86c03a435faa6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564770"
---
# <a name="canceling-a-notification"></a>Cancelar uma notificação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para cancelar uma notificação, clientes chame método de **Unadvise** de uma fonte advise. Chamar **Unadvise** é importante, porque ele faz com que o provedor de serviços liberar a sua referência para o seu coletor advise. Um provedor de serviço mantém uma referência para um coletor advise, desde que o coletor de eventos advise pode continuar a receber chamadas de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) . Na verdade, devido à natureza assíncrona da notificação de evento, clientes podem ser notificados mesmo depois de chamar um bem-sucedida **Unadvise** . Clientes devem estar aptos a lidar com o recebimento de notificações a qualquer momento. 
  
Como diferem de implementações de provedor de serviço, a clientes que falham ao **Unadvise** para cancelar uma notificação de chamada não podem assumir-nada sobre, quando um provedor lançará sua referência para seu coletor de eventos advise. Alguns provedores de serviços release suas referências para avisar PIAs quando eles liberam suas fontes advise. Alguns provedores de serviços tem não. Desde que um provedor de serviço mantém uma referência para um coletor advise, o coletor de eventos que advise pode continuar a receber notificações. 
  

