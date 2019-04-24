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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fbb05efff67fa90c68db86249d4657e489e7bd63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342774"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define o status associado a uma mensagem (por exemplo, se a mensagem está marcada para exclusão).
  
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
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada da mensagem cujo status é definido.
    
 _ulNewStatus_
  
> no O novo status a ser atribuído. 
    
 _ulNewStatusMask_
  
> no Uma bitmask de sinalizadores que é aplicada ao novo status e indica os sinalizadores a serem definidos. Os seguintes sinalizadores podem ser definidos:
    
MSGSTATUS_DELMARKED 
  
> A mensagem foi marcada para exclusão.
    
MSGSTATUS_HIDDEN 
  
> A mensagem não deve ser exibida.
    
MSGSTATUS_HIGHLIGHTED 
  
> A mensagem deve ser exibida em destaque.
    
MSGSTATUS_REMOTE_DELETE 
  
> A mensagem foi marcada para exclusão no armazenamento remoto de mensagens sem baixar para o cliente local.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> A mensagem foi marcada para download no repositório de mensagens remotas para o cliente local.
    
MSGSTATUS_TAGGED 
  
> A mensagem foi marcada para uma finalidade definida pelo cliente.
    
 _lpulOldStatus_
  
> bota Um ponteiro para o status anterior da mensagem.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O status da mensagem foi definido com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder:: SetMessageStatus** define o status da mensagem para o valor armazenado na sua propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Como os bits de status de mensagem são definidos, limpos e usados dependem completamente da sua implementação, exceto pelo fato de que os bits 0 a 15 são reservados e devem ser zero. 
  
A implementação de um provedor de transporte remoto desse método deve seguir as semânticas descritas aqui. Não há considerações especiais. Os clientes usam esse método para definir os bits MSGSTATUS_REMOTE_DOWNLOAD e MSGSTATUS_REMOTE_DELETE para indicar que uma determinada mensagem deve ser baixada ou excluída do repositório de mensagens remoto. Um provedor de transporte remoto não precisa implementar o método [IMAPIFolder:: GetMessageStatus](imapifolder-getmessagestatus.md) relacionado. Os clientes devem procurar na tabela de conteúdo da pasta para determinar o status de uma mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a propriedade **PR_MSG_STATUS** de uma mensagem para negociar uma operação de bloqueio de mensagens com outros clientes. Designar um bit como o bit de bloqueio. Para determinar se o bit de bloqueio foi definido, examine o valor anterior para status da mensagem no parâmetro _lpulOldStatus_ . Use os outros bits no parâmetro _ulNewStatus_ para rastrear o status da mensagem sem interferir no bit de bloqueio. 
  
## <a name="see-also"></a>Confira também



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

