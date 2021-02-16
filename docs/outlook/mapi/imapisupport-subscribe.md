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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419923"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra um evento de aviso para receber notificações por meio de MAPI.
  
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
  
> [in] Um ponteiro para uma chave de notificação que representa o objeto de origem de aviso. O  _parâmetro lpKey_ não pode ser NULL. 
    
 _ulEventMask_
  
> [in] Uma máscara de valores que indicam os tipos de eventos de notificação nos quais o chamador está interessado e devem ser incluídos no registro. Os seguintes valores são válidos:
    
 _fnevCriticalError_
  
> Registra notificações sobre erros graves, como memória insuficiente.
    
 _fnevExtended_
  
> Registra notificações sobre eventos específicos para o determinado address book ou provedor de armazenamento de mensagens.
    
 _fnevNewMail_
  
> Registra notificações sobre a chegada de novas mensagens. 
    
 _fnevObjectCreated_
  
> Registra notificações sobre a criação de um novo objeto.
    
 _fnevObjectCopied_
  
> Registra notificações sobre um objeto sendo copiado.
    
 _fnevObjectDeleted_
  
> Registra notificações sobre um objeto que está sendo excluído.
    
 _fnevObjectModified_
  
> Registra notificações sobre um objeto que está sendo modificado.
    
 _fnevObjectMoved_
  
> Registra notificações sobre um objeto que está sendo movido.
    
 _fnevSearchComplete_
  
> Registra notificações sobre a conclusão de uma operação de pesquisa.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a notificação ocorre. O sinalizador a seguir pode ser definido:
    
NOTIFY_SYNC 
  
> Quando o chamador chama o método [IMAPISupport::Notify](imapisupport-notify.md) para gerar notificações para esse pia de **aviso,** notificar deve fazer todas as chamadas necessárias para avisar os sinks antes de retornar. Se esse sinalizador não estiver definido, a notificação será assíncrona e os retornos de chamada serão ensuados para os processos que assinaram e iniciaram quando esses processos ganharem o controle da CPU. 
    
 _lpAdviseSink_
  
> [in] Um ponteiro para um objeto de evento de aconselhá-lo. 
    
 _lpulConnection_
  
> [out] Um ponteiro para um número de conexão que não seja zero que representa o registro.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro de notificação foi bem-sucedido.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::Subscribe** é implementado para todos os objetos de suporte do provedor de serviços. Os provedores de serviços **chamam Subscribe** de um dos métodos **Advise** para permitir que o MAPI gerencie as notificações. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para usar os métodos de suporte MAPI para notificação, crie uma chave para a fonte de avisos sobre o objeto sobre o qual as notificações devem ser geradas. O valor da chave deve ser exclusivo e ser facilmente regenerado sempre que o objeto mudar. 
  
MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source. Passe essa chave para **IMAPISupport::Notify** sempre que precisar gerar uma notificação para a fonte de aviso correspondente. 
  
O NOTIFY_SYNC sinalizador afeta a operação de chamadas subsequentes para **Notificar.** Quando você definir NOTIFY_SYNC, o **notify** não retornará até que ele termine de enviar todas as notificações necessárias. Quando você não definir o NOTIFY_SYNC, o **notify** opera de forma assíncrona, possivelmente retornando antes que todas as notificações tenham sido enviadas. 
  
## <a name="see-also"></a>Confira também



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[NOTIFICAÇÃO](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

