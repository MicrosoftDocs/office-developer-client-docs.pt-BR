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
ms.openlocfilehash: 8b15f12c9a7ac2041c895b935098f9681e4b3a3c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589949"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que o provedor de armazenamento de mensagem executar o processamento em uma mensagem enviada. Este método é chamado somente pelo spooler MAPI.
  
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
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da mensagem a ser processado.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Processamento na mensagem enviada foi bem-sucedida.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de armazenamento de mensagem não suporta o processamento da mensagem enviada. Esse valor de erro será retornado se o chamador não é o spooler MAPI.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore::FinishedMsg** realiza processamento em uma mensagem enviada. Esse processamento pode envolver excluindo a mensagem, movê-lo para uma pasta diferente, ou ambas as ações. O tipo de processamento depende se o **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) e as propriedades de **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) estão definidas. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Na sua implementação do **FinishedMsg**, desbloquear a mensagem identificada pela _lpEntryID_ e execute o processamento apropriado. A mensagem de destino sempre será bloqueada; o MAPI spooler nunca passa o identificador de entrada de mensagem desbloqueada para **FinishedMsg**.
  
É possível que nem **PR_DELETE_AFTER_SUBMIT** ou **PR_SENTMAIL_ENTRYID** estiver definida, ambos são definidos ou um ou outro estiver definido. A tabela a seguir descreve a ação que deve ser adotada com base nas configurações: 
  
|||
|:-----|:-----|
|Se nenhuma propriedade for definida:  <br/> |Deixe a mensagem na pasta da qual ela foi enviada (normalmente a caixa de saída).  <br/> |
|Se ambas as propriedades são definidas:  <br/> |Move a mensagem para a pasta indicada, se desejado e, em seguida, excluí-lo.  <br/> |
|Se estiver definido PR_SENTMAIL_ENTRYID:  <br/> |Move a mensagem para a pasta indicada.  <br/> |
|Se estiver definido PR_DELETE_AFTER_SUBMIT:  <br/> |Exclua a mensagem.  <br/> |
   
Depois de executar qualquer ação é apropriada, chame o método de [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

