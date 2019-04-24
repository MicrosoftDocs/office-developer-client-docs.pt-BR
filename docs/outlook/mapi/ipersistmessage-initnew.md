---
title: IPersistMessageInitNew
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.InitNew
api_type:
- COM
ms.assetid: 4bf37c35-4f72-438a-912c-402f3711a5ea
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317147"
---
# <a name="ipersistmessageinitnew"></a>IPersistMessage::InitNew

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicializa uma nova mensagem.
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parâmetros

 _pMessageSite_
  
> no Um ponteiro para o site de mensagens que o formulário usará para trabalhar com a mensagem no visualizador.
    
 _pMessage_
  
> no Um ponteiro para a nova mensagem.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A nova mensagem foi inicializada com êxito.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IPersistMessage:: InitNew** quando o usuário grava uma nova mensagem que pertence a uma classe de mensagem que o formulário manipula. Se o objeto Form tiver um ponteiro de interface do usuário válido, a interface do usuário para o objeto Message deverá ser exibida. 
  
 **InitNew** não deve ser chamado quando o formulário está em qualquer Estado, exceto [](uninitialized-state.md) o estado não inicializado. Se o formulário estiver em um dos outros Estados quando **InitNew** for chamado, retorne E_UNEXPECTED. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Normalmente, as mensagens que têm propriedades não salvas são marcadas como modificadas para que o cliente possa exibir uma caixa de diálogo solicitando ao usuário se essas propriedades devem ser salvas. Se o usuário indicar que uma mensagem deve ser salva, salve os dados, marque a mensagem como limpa e saia normalmente.
  
No enTanto, se o processamento de suas mensagens recentemente inicializadas incluir a configuração de uma ou mais propriedades computadas, e for importante que essas propriedades sejam salvas, não marque as mensagens como modificadas. Como as propriedades computadas devem ser invisíveis aos usuários, nenhuma caixa de diálogo deve ser exibida.
  
Se o formulário tiver uma referência a um site de mensagem ativo diferente daquele que é passado no **InitNew**, libere o site original porque ele não será mais usado. Armazene os ponteiros no site da mensagem e a mensagem dos parâmetros _pMessageSite_ e _PMessage_ e chame os métodos [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) dos dois objetos para incrementar suas contagens de referência. 
  
Defina as propriedades **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) e **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) para a nova mensagem para algo apropriado para sua classe de mensagem. Muitas classes de mensagens, por exemplo, define **PR_MESSAGE_FLAGS** como MSGFLAG_UNSENT para novas mensagens. 
  
Antes de retornar, migre o formulário para o estado [normal](normal-state.md) se nenhum erro tiver ocorrido. Envie uma nova notificação de mensagem para todos os visualizadores registrados chamando seus métodos [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) e retorne S_OK. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Depois de fazer uma chamada bem-sucedida para o **InitNew**, você pode supor que as seguintes propriedades obrigatórias e nenhuma outra tenham sido definidas para o formulário:
  
 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
Para obter mais informações sobre os Estados dos formulários, confira [Estados de formulário](form-states.md). Para obter mais informações sobre como os objetos de armazenamento são inicializados, consulte o método [IPersistStorage:: InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>Confira também



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

