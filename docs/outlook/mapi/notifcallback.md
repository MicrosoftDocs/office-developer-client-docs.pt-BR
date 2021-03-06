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
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434015"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função de retorno de chamada que MAPI chama para enviar uma notificação de evento. Essa função de retorno de chamada só pode ser usada quando envolvida em um objeto sink de alerta criado chamando a [função HrAllocAdviseSink.](hrallocadvisesink.md) 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Função definida implementada por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
|Função definida chamada por:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parâmetros

 _lpvContext_
  
> [in] Ponteiro para um valor arbitrário passado para a função de retorno de chamada quando MAPI o chama. Esse valor pode representar um endereço de significância para o aplicativo cliente ou provedor de serviços. Normalmente, para código C++, o parâmetro  _lpvContext_ representa um ponteiro para um objeto C++. 
    
 _cNotification_
  
> [in] Contagem de notificações de evento na matriz indicada pelo parâmetro _lpNotifications._ 
    
 _lpNotifications_
  
> [out] Ponteiro para o local onde essa função grava uma matriz de estruturas [notification](notification.md) que contém as notificações de evento. 
    
## <a name="return-value"></a>Valor de retorno

O conjunto de valores de retorno válidos para o protótipo da função **NOTIFCALLBACK** depende se a função é implementada por um aplicativo cliente ou um provedor de serviços. Os clientes sempre devem retornar S_OK. Os provedores podem retornar S_OK ou CALLBACK_DISCONTINUE. 
  
## <a name="remarks"></a>Comentários

CALLBACK_DISCONTINUE é um valor de retorno válido apenas para funções de retorno de chamada síncronas; solicita que o MAPI pare imediatamente o processamento dos retornos de chamada para essa notificação. Quando CALLBACK_DISCONTINUE é retornado, MAPI define o parâmetro  _lpUlFlags_ como NOTIFY_CANCELED quando retorna de [IMAPISupport::Notify](imapisupport-notify.md). 
  
A seguir estão limitações sobre o que uma função de retorno de chamada síncrona pode fazer:
  
- Ela não pode fazer com que outra notificação síncrona seja gerada.
    
- Ele não pode exibir uma interface do usuário.
    
## <a name="see-also"></a>Confira também



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

