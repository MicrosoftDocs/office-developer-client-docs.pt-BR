---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9e7d7ba91791258eca93a2b8bedf95cf121062c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427084"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que o provedor de armazenamento de mensagens execute o processamento em uma mensagem enviada. Esse método é chamado apenas pelo spooler MAPI.
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _cbEntryID_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da mensagem a ser processada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O processamento da mensagem enviada foi bem-sucedido.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de armazenamento de mensagens não dá suporte ao processamento de mensagens enviadas. Esse valor de erro será retornado se o chamador não for o spooler MAPI.
    
## <a name="remarks"></a>Comentários

O **método IMsgStore::FinishedMsg** executa o processamento em uma mensagem enviada. Esse processamento pode envolver a exclusão da mensagem, a movimentação para uma pasta diferente ou ambas as ações. O tipo de processamento depende se as propriedades **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) e **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) estão definidas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Na implementação de **FinishedMsg,** desbloqueie a mensagem identificada por  _lpEntryID_ e execute o processamento apropriado. A mensagem de destino sempre será bloqueada; o spooler MAPI nunca passa o identificador de entrada de uma mensagem desbloqueada para **FinishedMsg**.
  
É possível que **nenhum** PR_DELETE_AFTER_SUBMIT ou **PR_SENTMAIL_ENTRYID** seja definido, ambos estão definidos ou um ou outro está definido. A tabela a seguir descreve a ação que você deve tomar com base nas configurações: 
  
|||
|:-----|:-----|
|Se nenhuma das propriedades estiver definida:  <br/> |Deixe a mensagem na pasta da qual ela foi enviada (normalmente a Caixa de Saída).  <br/> |
|Se ambas as propriedades estão definidas:  <br/> |Mova a mensagem para a pasta indicada, se desejado, e exclua-a.  <br/> |
|Se PR_SENTMAIL_ENTRYID estiver definido:  <br/> |Mova a mensagem para a pasta indicada.  <br/> |
|Se PR_DELETE_AFTER_SUBMIT estiver definido:  <br/> |Exclua a mensagem.  <br/> |
   
Depois de tomar qualquer ação apropriada, chame o [método IMAPISupport::D oSentMail.](imapisupport-dosentmail.md) 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

