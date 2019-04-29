---
title: IMsgStoreAbortSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414379"
---
# <a name="imsgstoreabortsubmit"></a>IMsgStore::AbortSubmit

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Tenta remover uma mensagem da fila de saída.
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada da mensagem a ser removida da fila de saída. 
    
 _ulFlags_
  
> no Serve deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A mensagem foi removida com êxito da fila de saída.
    
MAPI_E_NOT_IN_QUEUE 
  
> A mensagem identificada por _lpEntryID_ não está mais na fila de saída do repositório de mensagens, geralmente porque já foi enviada. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> A mensagem identificada por _lpEntryID_ é bloqueada pelo spooler MAPI, e a operação não pode ser anulada. 
    
## <a name="remarks"></a>Comentários

O método **IMsgStore:: AbortSubmit** tenta remover uma mensagem enviada da fila de saída do armazenamento de mensagens. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Depois que uma mensagem é enviada, a anulação do envio chamando **AbortSubmit** é a única ação que pode ser executada na mensagem. Não espere que o **AbortSubmit** sempre seja bem-sucedido. Dependendo de como o sistema de mensagens subjacente é implementado, talvez não seja possível cancelar o envio da mensagem. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnAbortSubmit  <br/> |MFCMAPI usa o método **IMsgStore:: AbortSubmit** para anular o envio da mensagem selecionada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

