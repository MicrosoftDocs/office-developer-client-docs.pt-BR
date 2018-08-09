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
ms.openlocfilehash: bac363183c15a2d53c15b46724266b6cb5744075
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766982"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**Aplica-se a**: Outlook 
  
Obtém o status associado a uma mensagem em uma pasta particular (por exemplo, se a mensagem é marcada para exclusão).
  
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
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da mensagem cujo status é obtido.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulMessageStatus_
  
> [out] Um ponteiro para um ponteiro para uma bitmask dos sinalizadores que indicam o status da mensagem. Bits de 0 a 15 são reservados e devem ser zero; bits 16 a 31 estarão disponíveis para uso específico de implementação. Sinalizadores a seguir podem ser definidos:
    
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
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O status da mensagem foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder::GetMessageStatus** retorna o status de uma mensagem. Status da mensagem é armazenado na propriedade de **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Como os bits de status da mensagem estiver definidos, desmarcados e usados dependem completamente a implementação, exceto que os bits de 0 a 15 são reservados e devem ser zero. Se você armazenar mensagens na subárvore IPM, MAPI reserva bits 16 a 31 para uso por clientes IPM. Se você armazenar mensagens em outros subárvores, você pode usar o bits 16 a 31 para fins de seus próprios.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetNextMessage  <br/> |MFCMAPI usa o método **IMAPIFolder::GetMessageStatus** para obter o status da mensagem próximo a ser exibido.  <br/> |
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal e OpenMessageModal  <br/> |MFCMAPI usa o método **IMAPIFolder::GetMessageStatus** para obter o status da mensagem a ser exibido para passar para a tela de formulário, que é CMyMAPIFormViewer ou [IMAPISession:: ShowForm](imapisession-showform.md).  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

