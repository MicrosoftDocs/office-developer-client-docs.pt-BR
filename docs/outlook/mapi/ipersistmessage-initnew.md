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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394878"
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
  
> [in] Um ponteiro para o site de mensagem que o formulário usará para trabalhar com a mensagem no visualizador.
    
 _pMessage_
  
> [in] Um ponteiro para a nova mensagem.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A nova mensagem foi inicializada com êxito.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IPersistMessage::InitNew** quando o usuário escreve uma nova mensagem que pertence a uma classe de mensagem que processa o formulário. Se o objeto de formulário tiver um ponteiro de interface de usuário válido, a interface do usuário para o objeto de mensagem deve ser exibida. 
  
 **InitNew** não deve ser chamado quando o formulário estiver em qualquer estado, exceto o estado [não inicializado](uninitialized-state.md) . Se o formulário estiver em um dos outros estados quando **InitNew** é chamado, retorne E_UNEXPECTED. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Normalmente, as mensagens que não foram salvas propriedades são marcadas como modificado para que o cliente pode exibir uma caixa de diálogo que solicita ao usuário se essas propriedades devem ser salvas. Se o usuário indica que uma mensagem deve ser salvo, salvar os dados, marcar a mensagem como limpa e saia normalmente.
  
No entanto, se o processamento de suas mensagens recentemente inicializados inclui a definição de uma ou mais computado propriedades e é importante que essas propriedades a serem salvos, não marca as mensagens como modificado. Porque computados propriedades devem ser visíveis aos usuários, nenhuma caixa de diálogo deve ser exibida.
  
Se o seu formulário tem uma referência a um site da mensagem ativa diferente daquela que é passado para **InitNew**, libere o site original porque ele não será usado. Armazene os ponteiros para o site de mensagem e a mensagem de que os parâmetros _pMessageSite_ e _pMessage_ e chamar métodos de [AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) dos objetos para incrementar seus contagens de referência. 
  
Defina as propriedades de **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da nova mensagem e o **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) para algo apropriado para sua classe de mensagem. Muitas classes de mensagem, por exemplo, defina **PR_MESSAGE_FLAGS** como MSGFLAG_UNSENT para novas mensagens. 
  
Antes de retornar, a transição do formulário para o estado [Normal](normal-state.md) , se nenhum erro ocorreu. Enviar uma notificação de mensagem nova para todos os visualizadores registrados chamando os métodos [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) e retornar S_OK. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Depois de fazer uma chamada bem sucedida a **InitNew**, você pode assumir que as seguintes propriedades necessárias e nenhum outro foram definidos para o formulário:
  
 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
Para obter mais informações sobre os estados de formulários, consulte [Estados de formulário](form-states.md). Para obter mais informações sobre como os objetos de armazenamento são inicializados, consulte o método [IPersistStorage::InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>Confira também



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

