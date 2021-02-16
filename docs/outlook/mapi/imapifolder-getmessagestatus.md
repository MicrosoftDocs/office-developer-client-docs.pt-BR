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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418635"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obtém o status associado a uma mensagem em uma pasta específica (por exemplo, se essa mensagem está marcada para exclusão).
  
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
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da mensagem cujo status é obtido.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulMessageStatus_
  
> [out] Um ponteiro para um ponteiro para uma máscara de bits de sinalizadores que indicam o status da mensagem. Os bits de 0 a 15 são reservados e devem ser zero; os bits 16 a 31 estão disponíveis para uso específico da implementação. Os sinalizadores a seguir podem ser definidos:
    
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
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O status da mensagem foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPIFolder::GetMessageStatus** retorna o status de uma mensagem. O status da mensagem é armazenado na propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

A maneira como os bits de status da mensagem são definidos, limpos e usados depende completamente da implementação, exceto pelo fato de que os bits de 0 a 15 são reservados e devem ser zero. Se você armazenar mensagens na subárvore do IPM, o MAPI reserva bits de 16 a 31 para uso por clientes IPM. Se você armazenar mensagens em outras subárvore, poderá usar os bits 16 a 31 para suas próprias finalidades.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetNextMessage  <br/> |MFCMAPI usa o **método IMAPIFolder::GetMessageStatus** para obter o status da próxima mensagem a ser exibida.  <br/> |
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal e OpenMessageModal  <br/> |MFCMAPI usa o método **IMAPIFolder::GetMessageStatus** para obter o status da mensagem a ser exibida para passar para o visualizador de formulário, que é CMyMAPIFormViewer ou [IMAPISession::ShowForm](imapisession-showform.md).  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[Propriedade canônica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

