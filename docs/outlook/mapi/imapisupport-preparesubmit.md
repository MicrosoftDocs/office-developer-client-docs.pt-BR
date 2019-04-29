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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 738eb346ec5388cbd94b32598236ef2ca05740f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425733"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Prepara uma mensagem para envio ao spooler MAPI.
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpMessage_
  
> no Um ponteiro para a mensagem a ser preparada.
    
 _lpulFlags_
  
> [in, out] Na entrada, o parâmetro _lpulFlags_ é reservado e deve ser zero. Na saída, _lpulFlags_ deve ser nulo. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A mensagem foi preparada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::P reparesubmit** é implementado para objetos de suporte do provedor de repositório de mensagens. Os provedores de repositório de mensagens chamam **PrepareSubmit** em sua implementação do método [IMessage:: SubmitMessage](imessage-submitmessage.md) para preparar uma mensagem para envio ao spooler MAPI. 
  
 **PrepareSubmit** é usado para lidar com mensagens que têm o sinalizador MSGFLAG_RESEND definido em sua propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). MSGFLAG_RESEND é definido para mensagens que incluem uma solicitação a ser reenviada quando uma transmissão inicial falha. **PrepareSubmit** determina quais dos destinatários na lista de destinatários receberam com êxito a mensagem e que não o fizeram. 
  
Para acessar a lista de destinatários, **PrepareSubmit** chama o método [IMessage::](imessage-getrecipienttable.md) GetRecipientTable da mensagem. Para recuperar os dados do destinatário, **PrepareSubmit** chama o método IMAPITable [:: QueryRows](imapitable-queryrows.md) da tabela de destinatários. Para cada linha na tabela, **PrepareSubmit** verifica a propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) e executa uma das seguintes ações:
  
- Se o sinalizador MAPI_SUBMITTED estiver definido, **PrepareSubmit** limpará o sinalizador e definirá a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) como false.
    
- Se o sinalizador MAPI_SUBMITTED não estiver definido, **PrepareSubmit** altera **PR_RECIPIENT_TYPE** para MAPI_P1 e define **PR_RESPONSIBILITY** como true. 
    
## <a name="notes-to-callers"></a>Notas para chamadores

Antes de chamar o **PrepareSubmit**, certifique-se de que você chamou o método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) e defina o sinalizador NOTIFY_READYTOSEND no parâmetro _parâmetroulflags_ . A chamada **SpoolerNotify** deve ser feita uma vez por sessão antes da chamada para **PrepareSubmit**. O **SpoolerNotify** sincroniza o spooler MAPI e garante que todos os provedores de transporte necessários estejam conectados e que seus tipos de endereço sejam registrados. 
  
## <a name="see-also"></a>Confira também



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

