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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417270"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define o status associado a uma mensagem (por exemplo, se essa mensagem está marcada para exclusão).
  
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
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da mensagem cujo status está definido.
    
 _ulNewStatus_
  
> [in] O novo status a ser atribuído. 
    
 _ulNewStatusMask_
  
> [in] Uma máscara de bits de sinalizadores que é aplicada ao novo status e indica os sinalizadores a serem definidos. Os sinalizadores a seguir podem ser definidos:
    
MSGSTATUS_DELMARKED 
  
> A mensagem foi marcada para exclusão.
    
MSGSTATUS_HIDDEN 
  
> A mensagem não deve ser exibida.
    
MSGSTATUS_HIGHLIGHTED 
  
> A mensagem deve ser exibida realçada.
    
MSGSTATUS_REMOTE_DELETE 
  
> A mensagem foi marcada para exclusão no armazenamento de mensagens remoto sem ser baixada para o cliente local.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> A mensagem foi marcada para download do armazenamento de mensagens remoto para o cliente local.
    
MSGSTATUS_TAGGED 
  
> A mensagem foi marcada para uma finalidade definida pelo cliente.
    
 _lpulOldStatus_
  
> [out] Um ponteiro para o status anterior da mensagem.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O status da mensagem foi definido com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPIFolder::SetMessageStatus** define o status da mensagem como o valor armazenado em sua **propriedade PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

A maneira como os bits de status da mensagem são definidos, limpos e usados depende completamente da implementação, exceto que os bits de 0 a 15 são reservados e devem ser zero. 
  
A implementação desse método de um provedor de transporte remoto deve seguir a semântica descrita aqui. Não há considerações especiais. Os clientes usam esse método para definir os bits MSGSTATUS_REMOTE_DOWNLOAD e MSGSTATUS_REMOTE_DELETE bits para indicar que uma mensagem específica deve ser baixada ou excluída do armazenamento de mensagens remoto. Um provedor de transporte remoto não precisa implementar o [método IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) relacionado. Os clientes devem procurar na tabela de conteúdo da pasta para determinar o status de uma mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a **PR_MSG_STATUS** de uma mensagem para negociar uma operação de bloqueio de mensagem com outros clientes. Designe um pouco como o bit de bloqueio. Para determinar se o bit de bloqueio foi definido, examine o valor anterior para o status da mensagem no parâmetro _lpulOldStatus._ Use os outros bits no  _parâmetro ulNewStatus_ para rastrear o status da mensagem sem interferir no bit de bloqueio. 
  
## <a name="see-also"></a>Confira também



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

