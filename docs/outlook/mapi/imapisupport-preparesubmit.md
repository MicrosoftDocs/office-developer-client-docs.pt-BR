---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f6902b45cde3e5349d69b6f35c3f8980deb031b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767293"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

  
  
**Aplica-se a**: Outlook 
  
Prepara uma mensagem para o envio para o spooler MAPI.
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpMessage_
  
> [in] Um ponteiro para a mensagem para preparar.
    
 _lpulFlags_
  
> [além, out] Na entrada, o parâmetro _lpulFlags_ é reservado e deve ser zero. Na saída, _lpulFlags_ deve ser NULL. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A mensagem foi preparada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::PrepareSubmit** é implementado para objetos de suporte do provedor de repositório de mensagem. Provedores de armazenamento de mensagem chamarem **PrepareSubmit** em sua implementação do método [IMessage::SubmitMessage](imessage-submitmessage.md) para preparar uma mensagem para o envio para o spooler MAPI. 
  
 **PrepareSubmit** é usado para tratar mensagens que têm o sinalizador MSGFLAG_RESEND definido em sua propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). MSGFLAG_RESEND é definida para mensagens que incluem uma solicitação a ser reenviado quando uma transmissão inicial falha. **PrepareSubmit** determina qual dos destinatários na lista de destinatários com êxito recebeu a mensagem e que não especificou. 
  
Para acessar a lista de destinatários, **PrepareSubmit** chama o método de [IMessage::GetRecipientTable](imessage-getrecipienttable.md) da mensagem. Para recuperar os dados de destinatário, **PrepareSubmit** chama o método [IMAPITable:: QueryRows](imapitable-queryrows.md) de destinatário da tabela. Para cada linha na tabela, **PrepareSubmit** verifica a propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) e usa uma das seguintes ações:
  
- Se o sinalizador MAPI_SUBMITTED estiver definido, o **PrepareSubmit** limpa o sinalizador e define a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) como FALSE.
    
- Se o sinalizador MAPI_SUBMITTED não estiver definido, o **PrepareSubmit** **PR_RECIPIENT_TYPE** é alterado para MAPI_P1 e define **PR_RESPONSIBILITY** como TRUE. 
    
## <a name="notes-to-callers"></a>Notas para chamadores

Antes de chamar **PrepareSubmit**, certifique-se de que você chamou o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) e definir o sinalizador NOTIFY_READYTOSEND no parâmetro _ulFlags_ . A chamada **SpoolerNotify** deve ser feita uma vez por sessão antes da chamada para **PrepareSubmit**. **SpoolerNotify** sincroniza o MAPI spooler e garante que todos os provedores de transporte needed estiver conectados e seus tipos de endereço são registrados. 
  
## <a name="see-also"></a>Confira também



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

