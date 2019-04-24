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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9eeede2a430f5186daf429dd6ed59f312ae334be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348745"
---
# <a name="imsgstoresetlockstate"></a>IMsgStore::SetLockState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Bloqueia ou desbloqueia uma mensagem. Este método é chamado apenas pelo spooler MAPI.
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a>Parâmetros

 _lpMessage_
  
> no Um ponteiro para a mensagem a ser bloqueada ou desbloqueada.
    
 _ulLockState_
  
> no Um valor que indica se a mensagem deve ser bloqueada ou desbloqueada. Um dos seguintes valores é válido:
    
MSG_LOCKED 
  
> A mensagem deve ser bloqueada. 
    
MSG_UNLOCKED 
  
> A mensagem deve ser desbloqueada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O estado de bloqueio da mensagem foi definido com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore::** setlockstate bloqueia ou desbloqueia uma mensagem. **** Setlockstate só pode ser chamado pelo spooler MAPI enquanto ele está enviando a mensagem. 
  
Normalmente, quando o spooler MAPI chama setLockstate para bloquear uma mensagem, ele bloqueia somente a mensagem mais antiga (ou seja, a próxima mensagem enfileirada para o spooler MAPI a ser enviado). **** Se a mensagem mais antiga na fila estiver aguardando um provedor de transporte temporariamente indisponível e a próxima mensagem na fila usar um provedor de transporte diferente, o spooler MAPI poderá começar a processar a mensagem mais tarde. Ele começa o processamento bloqueando essa mensagem usando **** setlockstate.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Após o spooler MAPI ter chamado setLockstate com o parâmetro _ulLockState_ definido como MSG_LOCKED, as chamadas para o método [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) para cancelar a transmissão da mensagem devem falhar. **** 
  
Chame o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da mensagem em sua **** implementação setlockstate para que quaisquer alterações feitas à mensagem antes da chamada setlockstate sejam salvas. **** 
  
## <a name="see-also"></a>Confira também



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

