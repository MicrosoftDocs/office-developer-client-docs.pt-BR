---
title: IXPLogonStartMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.StartMessage
api_type:
- COM
ms.assetid: 83c349f7-dcac-4268-befe-fb2bc0cd9c50
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3758cf72aa79dbf500138e96872352950fafbd2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767755"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**Aplica-se a**: Outlook 
  
Inicia a transferência de uma mensagem de entrada do provedor de transporte para o spooler MAPI.
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpMessage_
  
> [in] Um ponteiro para um objeto de mensagem (representando a mensagem de entrada) que tem permissão de leitura/gravação, que é usado pelo provedor de transporte para acessar e manipular a mensagem. Este objeto permanecerá válido até depois que o provedor de transporte retornará da chamada para **IXPLogon::StartMessage**.
    
 _lpulMsgRef_
  
> [out] Um ponteiro para um valor de referência atribuído à mensagem. O MAPI spooler inicializa esse valor como 1 antes que ele retorna o ponteiro para o provedor de transporte.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

O MAPI spooler chama o método **IXPLogon::StartMessage** para iniciar a transferência de uma mensagem de entrada do provedor de transporte para o spooler MAPI. Antes do provedor de transporte começa a usar a mensagem apontada pela _lpMessage_, ele deve armazenar uma referência de mensagem no parâmetro _lpulMsgRef_ para uso potencial por uma chamada ao método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) . 
  
Durante uma chamada de **StartMessage** , o MAPI spooler processa métodos para objetos abertos durante a transferência da mensagem, e também processa todos os anexos. Esse processamento pode levar muito tempo. Provedores de transporte podem chamar a função de retorno de chamada [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) para o MAPI spooler frequentemente durante o processamento para liberar o tempo da CPU para outras tarefas do sistema. 
  
Todos os destinatários na tabela de destinatário que cria um provedor de transporte para a mensagem devem conter todas as propriedades obrigatórias de endereçamento. Se necessário, o provedor pode construir um destinatário personalizado para representar um destinatário específico. No entanto, se o provedor pode gerar uma entrada do destinatário que inclui mais informações, ele deve fazer isso. Por exemplo, se um provedor de transporte tem informações suficientes sobre formato de destinatário de um provedor catálogo de endereços que ele pode construir um identificador de entrada válida para um destinatário para esse formato, ele deve construir o identificador de entrada.
  
Se todas as propriedades nontransmittable são recebidas, o provedor de transporte não deve armazená-los na nova mensagem. No entanto, o provedor de transporte deve armazenar todas as propriedades transmittable, que ele recebe na nova mensagem.
  
Se a mensagem de entrada é um relatório de entrega ou um relatório de não entrega e o provedor de transporte é possível utilizar o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para gerar o relatório a partir da mensagem original, o provedor, em si, deve popular a mensagem com as propriedades adequadas. No entanto, o provedor de transporte não pode definir a propriedade de **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da mensagem.
  
Para salvar a mensagem de entrada no armazenamento de mensagens MAPI apropriado após o processamento, o provedor de transporte chama o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Se o provedor de transporte não tem todas as mensagens a serem passados para o spooler MAPI, ele pode interromper a mensagem de entrada, retornando da chamada **StartMessage** sem chamar **SaveChanges**.
  
Todos os objetos que o provedor de transporte abre durante uma chamada de **StartMessage** devem ser liberados antes de retornar. No entanto, o provedor não deve liberar o objeto de mensagem que o MAPI spooler originalmente passado no parâmetro _lpMessage_ . 
  
Se **StartMessage** retornará um erro, a mensagem no processo for lançada sem ter que as alterações foram salvas e serão perdida. Nesse caso, o provedor de transporte deve passar o sinalizador NOTIFY_CRITICAL_ERROR com uma chamada para o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) e chame o método [IXPLogon::Poll](ixplogon-poll.md) para notificar o MAPI spooler que ele está em uma condição de erro grave. 
  
Para obter mais informações, consulte [interagindo com o Spooler de MAPI](interacting-with-the-mapi-spooler.md). 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

