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
ms.openlocfilehash: 36b8381e2bf98f5ddcb88a54b56f2b5c91b3b668
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572596"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Identifica exclusivamente uma conexão entre um coletor advise, uma fonte de advise e MAPI.
  
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
  
> Contagem de bytes no membro **ab** . 
    
 **AB**
  
> Matriz de bytes que descreve a chave de notificação.
    
## <a name="remarks"></a>Comentários

Os métodos [Subscribe](imapisupport-subscribe.md) e [Notificar](imapisupport-notify.md) do [IMAPISupport](imapisupportiunknown.md) usam a estrutura **NOTIFKEY** para gerar notificações para o coletor de advise apropriado sobre a fonte advise apropriado. 
  
Provedores de serviços geram chaves de notificação quando seu método **Advise** é chamado e eles desejam **inscrever-se** para lidar com o registro de notificação e o subsequentes envio de notificações de chamada. Uma chave de notificação pode ser o identificador de entrada da fonte de advise ou pode ser qualquer outro item de identificação, como uma constante. Por exemplo, um provedor de armazenamento de mensagem pode usar o caminho de uma pasta como sua chave de notificação. 
  
A chave de notificação deve funcionar em vários processos. 
  
Os requisitos de escopo para uma chave de notificação se parecem com aqueles para um identificador de entrada de longo prazo. No entanto, ao contrário de um identificador de entrada, uma chave de notificação deve ser binário-comparável. Normalmente, uma chave de notificação inclui um valor **GUID** definido pelo provedor de serviços seguido por outras informações específicas do provedor exclusivas ao objeto. 
  
Para uma discussão sobre o uso da estrutura de **NOTIFKEY** para gerenciar as conexões entre receptores de advise e os objetos que geram notificações, consulte [Suporte a notificação de evento](supporting-event-notification.md). 
  
## <a name="see-also"></a>Confira também



[Estruturas MAPI](mapi-structures.md)

