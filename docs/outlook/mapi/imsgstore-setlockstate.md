---
title: IMsgStoreSetLockState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetLockState
api_type:
- COM
ms.assetid: 4b1176ec-4126-43f5-856d-cbab8d622825
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2efee531e277b6295b7d4bc299eefc789a805d34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571084"
---
# <a name="imsgstoresetlockstate"></a>IMsgStore::SetLockState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Bloqueia ou desbloqueia uma mensagem. Este método é chamado somente pelo spooler MAPI.
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a>Parâmetros

 _lpMessage_
  
> [in] Um ponteiro para a mensagem para bloquear ou desbloquear.
    
 _ulLockState_
  
> [in] Um valor que indica se a mensagem deve ser bloqueada ou desbloqueada. Um dos valores a seguir é válido:
    
MSG_LOCKED 
  
> A mensagem deve ser bloqueada. 
    
MSG_UNLOCKED 
  
> A mensagem deve ser desbloqueada.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O estado de bloqueio da mensagem foi definido com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore::SetLockState** bloqueia ou desbloqueia uma mensagem. **SetLockState** pode ser chamado apenas pelo spooler MAPI enquanto ele está enviando a mensagem. 
  
Normalmente, quando o MAPI spooler chama **SetLockState** para bloquear uma mensagem, ele bloqueia somente a mensagem mais antiga (ou seja, a próxima mensagem na fila para o spooler MAPI enviar). Se a mensagem mais antiga na fila está aguardando para um provedor de transporte temporariamente indisponível e a próxima mensagem na fila usa um provedor de transporte diferentes, o MAPI spooler pode começar a processar a mensagem posterior. Ele começará processamento bloqueando mensagem usando **SetLockState**.
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Depois que o MAPI spooler tiver chamado **SetLockState** com o parâmetro _ulLockState_ definido como MSG_LOCKED, chamadas ao método [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para cancelar a transmissão da mensagem devem falhar. 
  
Chame o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem na sua implementação **SetLockState** para que quaisquer alterações que foram feitas à mensagem antes que a chamada **SetLockState** foi recebida sejam salvas. 
  
## <a name="see-also"></a>Confira também



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

