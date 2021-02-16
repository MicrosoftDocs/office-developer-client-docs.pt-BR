---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429625"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Identifica exclusivamente uma conexão entre um evento de aconselhamento, uma fonte de consultoria e MAPI.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a>Members

 **cb**
  
> Contagem de bytes no **membro ab.** 
    
 **ab**
  
> Matriz de bytes descrevendo a chave de notificação.
    
## <a name="remarks"></a>Comentários

Os [métodos Subscribe](imapisupport-subscribe.md) e [Notify](imapisupport-notify.md) de [IMAPISupport](imapisupportiunknown.md) usam a estrutura **NOTIFKEY** para gerar notificações para o pia de aviso apropriado sobre a fonte de aviso apropriada. 
  
Os provedores de serviços geram chaves de notificação  quando o método **Advise** é chamado e querem chamar Subscribe para manipular o registro de notificação e o envio subsequente de notificações. Uma chave de notificação pode ser o identificador de entrada da fonte de aviso ou pode ser qualquer outro item que identifique, como uma constante. Por exemplo, um provedor de armazenamento de mensagens pode usar o caminho de uma pasta como sua chave de notificação. 
  
A chave de notificação deve funcionar em vários processos. 
  
Os requisitos de escopo para uma chave de notificação são semelhantes aos de um identificador de entrada de longo prazo. No entanto, ao contrário de um identificador de entrada, uma chave de notificação deve ser comparável a binários. Normalmente, uma chave de notificação inclui um valor **GUID** definido pelo provedor de serviços seguido por outras informações específicas do provedor exclusivas do objeto. 
  
For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md). 
  
## <a name="see-also"></a>Confira também



[Estruturas MAPI](mapi-structures.md)

