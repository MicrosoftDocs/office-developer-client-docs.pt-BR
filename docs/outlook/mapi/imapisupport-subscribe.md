---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5a8c288e877078ece6ab2da8c6494d96e1714ad7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328948"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra um coletor de aviso para receber notificações por meio de MAPI.
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _lpKey_
  
> no Um ponteiro para uma chave de notificação que representa o objeto de origem de aviso. O parâmetro _lpKey_ não pode ser nulo. 
    
 _ulEventMask_
  
> no Uma máscara de valores que indica os tipos de eventos de notificação nos quais o chamador está interessado e deve ser incluído no registro. Os seguintes valores são válidos:
    
 _fnevCriticalError_
  
> Registra para notificações sobre erros graves, como memória insuficiente.
    
 _fnevExtended_
  
> Registra para notificações sobre eventos específicos para o catálogo de endereços ou o provedor de armazenamento de mensagens específico.
    
 _fnevNewMail_
  
> Registra as notificações sobre a chegada de novas mensagens. 
    
 _fnevObjectCreated_
  
> Registra as notificações sobre a criação de um novo objeto.
    
 _fnevObjectCopied_
  
> Registra para notificações sobre um objeto que está sendo copiado.
    
 _fnevObjectDeleted_
  
> Registra as notificações sobre um objeto que está sendo excluído.
    
 _fnevObjectModified_
  
> Registra para notificações sobre um objeto que está sendo modificado.
    
 _fnevObjectMoved_
  
> Registra as notificações sobre um objeto que está sendo movido.
    
 _fnevSearchComplete_
  
> Registra as notificações sobre a conclusão de uma operação de pesquisa.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam como a notificação ocorre. O seguinte sinalizador pode ser definido:
    
NOTIFY_SYNC 
  
> Quando o chamador chama o método [IMAPISupport:: Notify](imapisupport-notify.md) para gerar notificações para este coletor de aviso, **Notify** deve fazer todas as chamadas necessárias para avisar os coletores antes de retornar. Se esse sinalizador não for definido, a notificação será assíncrona e os retornos de chamada serão enfileirados para os processos que foram inscritos e iniciados quando esses processos ganharem controle da CPU. 
    
 _lpAdviseSink_
  
> no Um ponteiro para um objeto de coletor de aviso. 
    
 _lpulConnection_
  
> bota Um ponteiro para um número de conexão diferente de zero que representa o registro.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro de notificação foi bem-sucedido.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: Subscribe** é implementado para todos os objetos de suporte do provedor de serviços. Os provedores de serviços chamam a **assinatura** de um dos seus métodos de **aviso** para permitir que o MAPI gerencie as notificações. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para usar os métodos de suporte MAPI para notificação, crie uma chave para a fonte de aviso o objeto sobre quais notificações devem ser geradas. O valor da chave deve ser exclusivo e ser facilmente regenerado a cada vez que o objeto é alterado. 
  
MAPI usa a chave de notificação para procurar qualquer função de retorno de chamada registrada por meio da função [HrAllocAdviseSink](hrallocadvisesink.md) para a fonte de aviso correspondente. Passe essa chave para **IMAPISupport:: Notify** sempre que precisar gerar uma notificação para a fonte de aviso correspondente. 
  
O sinalizador NOTIFY_SYNC afeta a operação de chamadas subsequentes **** para notificar. Quando você define NOTIFY_SYNC, **Notify** não retorna até que o envio de todas as notificações necessárias seja concluído. Quando você não definir o NOTIFY_SYNC, **notificar** funciona de forma assíncrona, possivelmente retornando antes que todas as notificações tenham sido enviadas. 
  
## <a name="see-also"></a>Confira também



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[NOTIFICATION](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

