---
title: IMAPIFolderSetMessageStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: fcca6a7e8fa70a2df9042e8b3c2b28825cee9a7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766993"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**Aplica-se a**: Outlook 
  
Define o status associado a uma mensagem (por exemplo, se a mensagem é marcada para exclusão).
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da mensagem cujo status esteja definido.
    
 _ulNewStatus_
  
> [in] O novo status a ser atribuído. 
    
 _ulNewStatusMask_
  
> [in] Uma bitmask dos sinalizadores que é aplicada para o novo status e indica os sinalizadores a ser definido. Sinalizadores a seguir podem ser definidos:
    
MSGSTATUS_DELMARKED 
  
> A mensagem foi marcada para exclusão.
    
MSGSTATUS_HIDDEN 
  
> A mensagem não será exibido.
    
MSGSTATUS_HIGHLIGHTED 
  
> A mensagem deve ser exibida realçado.
    
MSGSTATUS_REMOTE_DELETE 
  
> A mensagem foi marcada para exclusão na loja remota de mensagens sem baixar no cliente local.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> A mensagem foi marcada para download a partir do armazenamento de mensagens remoto no cliente local.
    
MSGSTATUS_TAGGED 
  
> A mensagem foram marcada para uma finalidade definida pelo cliente.
    
 _lpulOldStatus_
  
> [out] Um ponteiro para o status anterior da mensagem.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O status da mensagem foi definido com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder::SetMessageStatus** define o status da mensagem com o valor armazenado na sua propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Como os bits de status da mensagem estiver definidos, desmarcados e usados dependem completamente a implementação, exceto que os bits de 0 a 15 são reservados e devem ser zero. 
  
Implementação de um provedor de transporte remoto deste método deve seguir a semântica descrita aqui. Não há nenhuma considerações especiais. Clientes usam esse método para definir os bits MSGSTATUS_REMOTE_DOWNLOAD e MSGSTATUS_REMOTE_DELETE para indicar que uma mensagem específica é a serem baixadas ou excluído do armazenamento remoto de mensagem. Não tem um provedor de transporte remoto implementar o método [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) relacionado. Os clientes devem procure na tabela de conteúdo da pasta para determinar o status de uma mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a propriedade **PR_MSG_STATUS** de uma mensagem para negociar uma operação de bloqueio de mensagem com outros clientes. Designe um pouco como o bit de bloqueio. Para determinar se foi definido o bit de bloqueio, examine o valor anterior para o status da mensagem no parâmetro _lpulOldStatus_ . Use os outros bits no parâmetro _ulNewStatus_ para acompanhar o status da mensagem sem interferir estará definido o bit bloqueio. 
  
## <a name="see-also"></a>Confira também



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

