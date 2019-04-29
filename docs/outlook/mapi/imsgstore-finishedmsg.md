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
  
Permite que o provedor de repositório de mensagens realize o processamento em uma mensagem enviada. Este método é chamado apenas pelo spooler MAPI.
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Serve deve ser zero.
    
 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada da mensagem a ser processada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O processamento da mensagem enviada foi bem-sucedido.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de repositório de mensagens não dá suporte ao processamento de mensagens enviadas. Este valor de erro será retornado se o chamador não for o MAPI spooler.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore:: FinishedMsg** executa o processamento em uma mensagem enviada. Esse processamento pode envolver a exclusão da mensagem, movê-la para uma pasta diferente ou ambas as ações. O tipo de processamento depende se as propriedades **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) e **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) estão definidas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Em sua implementação do **FinishedMsg**, desbloqueie a mensagem identificada por _lpEntryID_ e execute o processamento apropriado. A mensagem de destino sempre será bloqueada; o spooler MAPI nunca passa o identificador de entrada de uma mensagem desbloqueada para **FinishedMsg**.
  
É possível que nem **PR_DELETE_AFTER_SUBMIT** ou **PR_SENTMAIL_ENTRYID** estejam definidos, ambos estejam definidos ou um ou outro esteja definido. A tabela a seguir descreve a ação que deve ser executada com base nas configurações: 
  
|||
|:-----|:-----|
|Se nenhuma propriedade for definida:  <br/> |Deixe a mensagem na pasta a partir da qual ela foi enviada (normalmente, a).  <br/> |
|Se ambas as propriedades estiverem definidas:  <br/> |Mova a mensagem para a pasta indicada, se desejado, e, em seguida, exclua-a.  <br/> |
|Se PR_SENTMAIL_ENTRYID estiver definido:  <br/> |Mova a mensagem para a pasta indicada.  <br/> |
|Se PR_DELETE_AFTER_SUBMIT estiver definido:  <br/> |Exclua a mensagem.  <br/> |
   
Depois de ter feito qualquer ação apropriada, chame o método [IMAPISupport::D osentmail](imapisupport-dosentmail.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

