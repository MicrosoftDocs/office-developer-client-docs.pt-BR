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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6658f1c4bcfaf7557d9b53c5e70d87e124475580
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767317"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**Aplica-se a**: Outlook 
  
Registra um coletor advise para receber notificações por meio de MAPI.
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Par�metros

 _lpKey_
  
> [in] Um ponteiro para uma chave de notificação que representa o objeto de origem advise. O parâmetro _lpKey_ não pode ser NULL. 
    
 _ulEventMask_
  
> [in] Uma máscara de valores que indicam os tipos de eventos de notificação que o chamador está interessado em e deve ser incluído no registro. Os seguintes valores são válidos:
    
 _fnevCriticalError_
  
> Registradores para notificações sobre erros graves, como as de memória insuficiente.
    
 _fnevExtended_
  
> Provedor de armazenamento de registradores para notificações sobre eventos específicos ao catálogo de endereços particular ou mensagem.
    
 _fnevNewMail_
  
> Registradores para notificações sobre a chegada de novas mensagens. 
    
 _fnevObjectCreated_
  
> Registradores para notificações sobre a criação de um novo objeto.
    
 _fnevObjectCopied_
  
> Registradores para notificações sobre um objeto que está sendo copiada.
    
 _fnevObjectDeleted_
  
> Registradores para notificações sobre um objeto que está sendo excluído.
    
 _fnevObjectModified_
  
> Registradores para notificações sobre um objeto que está sendo modificado.
    
 _fnevObjectMoved_
  
> Registradores para notificações sobre um objeto que está sendo movido.
    
 _fnevSearchComplete_
  
> Registradores para notificações sobre a conclusão de uma operação de pesquisa.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como ocorre a notificação. O seguinte sinalizador pode ser definido:
    
NOTIFY_SYNC 
  
> Quando o chamador chama o método [IMAPISupport::Notify](imapisupport-notify.md) para gerar notificações para esse coletor advise, **Notify** deve fazer todas as chamadas necessárias aos receptores de aviso antes de retornar. Se esse sinalizador não estiver definida, notificação é assíncrona e retornos de chamada são enfileirados aos processos que tem se inscrito e iniciado quando esses processos assumir o controle da CPU. 
    
 _lpAdviseSink_
  
> [in] Um ponteiro para um objeto de coletor de eventos advise. 
    
 _lpulConnection_
  
> [out] Um ponteiro para um número diferente de zero de conexão que representa o registro.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O registro de notificação foi bem-sucedida.
    
## <a name="remarks"></a>Coment�rios

O método **IMAPISupport::Subscribe** é implementado para todos os objetos de suporte de provedor de serviço. Provedores de serviços chamarem **Subscribe** de um dos seus métodos **Advise** para permitir que o MAPI gerenciar as notificações. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para usar os métodos de suporte MAPI para fins de notificação, crie uma chave para a fonte de advise o objeto sobre o qual as notificações deve ser gerado. O valor da chave deve ser exclusivo e deve ser facilmente gerar toda vez que o objeto altera. 
  
MAPI usa a chave de notificação para procurar qualquer funções de retorno de chamada registradas por meio da função [HrAllocAdviseSink](hrallocadvisesink.md) para a fonte de advise correspondente. Passe essa chave para **IMAPISupport::Notify** sempre que precisar gerar uma notificação para a fonte de advise correspondente. 
  
O sinalizador NOTIFY_SYNC afeta a operação de chamadas subsequentes para **Notificar**. Quando você define NOTIFY_SYNC, **Notify** não retorna até que ele tenha terminado enviar todas as notificações necessárias. Quando você não definir NOTIFY_SYNC, **Notify** opera de forma assíncrona, retornando possivelmente antes de todas as notificações foram enviadas. 
  
## <a name="see-also"></a>Confira também



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[NOTIFICAÇÃO](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

