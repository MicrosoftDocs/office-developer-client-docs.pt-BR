---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b14529e987b85d1dcbe3689d4e852a9efd39a396
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768156"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**Aplica-se a**: Outlook 
  
Define uma função de retorno de chamada que chamadas MAPI para enviar uma notificação de evento. Essa função de retorno de chamada pode ser usada apenas quando disposto em um objeto de coletor de eventos advise criado chamando-se a função [HrAllocAdviseSink](hrallocadvisesink.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Função definido implementada por:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
|Função definido chamada pelo:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parâmetros

 _lpvContext_
  
> [in] Ponteiro para um valor arbitrário passado para a função de retorno de chamada quando chamadas de MAPI-lo. Esse valor pode representar um endereço de significância para o aplicativo cliente ou o provedor de serviço. Geralmente, para código C++, o parâmetro _lpvContext_ representa um ponteiro para um objeto C++. 
    
 _cNotification_
  
> [in] Contagem de notificações de evento na matriz indicado pelo parâmetro _lpNotifications_ . 
    
 _lpNotifications_
  
> [out] Ponteiro para o local onde essa função grava uma matriz de estruturas de [notificação](notification.md) que contém as notificações de evento. 
    
## <a name="return-value"></a>Valor retornado

O conjunto de valores de retorno válidos para o protótipo de função **NOTIFCALLBACK** depende se a função é implementada por um provedor de serviços ou de um aplicativo cliente. Clientes sempre devem retornar S_OK. Provedores podem retornar S_OK ou CALLBACK_DISCONTINUE. 
  
## <a name="remarks"></a>Comentários

CALLBACK_DISCONTINUE é um valor de retorno válido para funções de retorno de chamada síncrona apenas; ele solicita que o MAPI parar imediatamente os retornos de chamada para essa notificação de processamento. Quando CALLBACK_DISCONTINUE é retornado, MAPI define o parâmetro _lpUlFlags_ para NOTIFY_CANCELED quando ele retorna da [IMAPISupport::Notify](imapisupport-notify.md). 
  
A seguir estão limitações no que pode fazer uma função de retorno de chamada síncrona:
  
- Ele não pode causar outra notificação síncrona a serem gerados.
    
- Ele não pode exibir uma interface do usuário.
    
## <a name="see-also"></a>Confira também



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

