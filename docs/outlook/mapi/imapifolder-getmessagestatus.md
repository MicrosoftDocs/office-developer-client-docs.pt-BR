---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 621c20376cc671a2ff9d1406bfb6248846e1bc81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350950"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obtém o status associado a uma mensagem em uma pasta específica (por exemplo, se a mensagem está marcada para exclusão).
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada da mensagem cujo status é obtido.
    
 _ulFlags_
  
> no Serve deve ser zero.
    
 _lpulMessageStatus_
  
> bota Um ponteiro para um ponteiro para uma bitmask de sinalizadores que indicam o status da mensagem. Os bits de 0 a 15 são reservados e devem ser zero; os bits 16 a 31 estão disponíveis para uso específico da implementação. Os seguintes sinalizadores podem ser definidos:
    
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
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O status da mensagem foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder:: GetMessageStatus** retorna o status de uma mensagem. O status da mensagem é armazenado na propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Como os bits de status de mensagem são definidos, limpos e usados dependem completamente da sua implementação, exceto pelo fato de que os bits 0 a 15 são reservados e devem ser zero. Se você armazenar mensagens na sub-árvore IPM, o MAPI reserva bits 16 a 31 para uso por clientes IPM. Se você armazenar mensagens em outras subárvores, poderá usar bits de 16 a 31 para suas próprias finalidades.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: GetNextMessage  <br/> |MFCMAPI usa o método **IMAPIFolder:: GetMessageStatus** para obter o status da próxima mensagem a ser exibida.  <br/> |
|MAPIFormFunctions. cpp  <br/> |OpenMessageNonModal e OpenMessageModal  <br/> |MFCMAPI usa o método **IMAPIFolder:: GetMessageStatus** para obter o status da mensagem a ser exibida para passar para o Visualizador de formulários, que é CMyMAPIFormViewer ou [IMAPISession:: formulário](imapisession-showform.md).  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

