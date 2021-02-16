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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 00273d5572fa0c12a9501a1620db11ea087fd5d1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427602"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Um ponteiro para um objeto de mensagem (representando a mensagem de entrada) que tem permissão de leitura/gravação, que é usada pelo provedor de transporte para acessar e manipular essa mensagem. Esse objeto permanece válido até que o provedor de transporte retorne da chamada para **IXPLogon::StartMessage**.
    
 _lpulMsgRef_
  
> [out] Um ponteiro para um valor de referência atribuído à mensagem. O spooler MAPI inicializa esse valor como 1 antes de retornar o ponteiro para o provedor de transporte.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPLogon::StartMessage** para iniciar a transferência de uma mensagem de entrada do provedor de transporte para o spooler MAPI. Antes que o provedor de transporte comece a usar a mensagem apontada por _lpMessage_, ele deve armazenar uma referência de mensagem no parâmetro _lpulMsgRef_ para uso potencial por uma chamada para o método [IXPLogon::TransportNotify.](ixplogon-transportnotify.md) 
  
Durante uma **chamada StartMessage,** o spooler MAPI processa métodos para objetos abertos durante a transferência da mensagem e também processa todos os anexos. Esse processamento pode levar muito tempo. Provedores de transporte podem chamar a função de retorno de chamada [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) para o spooler MAPI frequentemente durante esse processamento para liberar tempo de CPU para outras tarefas do sistema. 
  
Todos os destinatários na tabela de destinatários que o provedor de transporte cria para a mensagem devem conter todas as propriedades de endereçamento necessárias. Se necessário, o provedor pode construir um destinatário personalizado para representar um destinatário específico. No entanto, se o provedor puder produzir uma entrada de destinatário que inclua mais informações, ele deverá fazê-lo. Por exemplo, se um provedor de transporte tiver informações suficientes sobre o formato de destinatário de um provedor de agendas para que possa criar um identificador de entrada válido para um destinatário para esse formato, ele deverá criar o identificador de entrada.
  
Se alguma propriedade nãotransmitível for recebida, o provedor de transporte não deverá armazená-las na nova mensagem. No entanto, o provedor de transporte deve armazenar todas as propriedades transmitíveis que receber na nova mensagem.
  
Se a mensagem de entrada for um relatório de entrega ou um relatório de não entrega e o provedor de transporte não puder usar o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para gerar o relatório a partir da mensagem original, o provedor deverá preencher a mensagem com as propriedades apropriadas. No entanto, o provedor de transporte não pode definir a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da mensagem.
  
Para salvar a mensagem de entrada no armazenamento de mensagens MAPI apropriado após o processamento, o provedor de transporte chama o método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Se o provedor de transporte não tiver nenhuma mensagem para passar para o spooler MAPI, ele poderá interromper a mensagem de entrada retornando da chamada **StartMessage** sem chamar **SaveChanges**.
  
Todos os objetos que o provedor de transporte abre durante uma **chamada StartMessage** devem ser liberados antes do retorno. No entanto, o provedor não deve liberar o objeto de mensagem que o spooler MAPI originalmente passou no _parâmetro lpMessage._ 
  
Se **StartMessage retornar** um erro, a mensagem em processo será liberada sem ter alterações salvas e será perdida. Nesse caso, o provedor de transporte deve passar o sinalizador NOTIFY_CRITICAL_ERROR com uma chamada para o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) e chamar o método [IXPLogon::P oll](ixplogon-poll.md) para notificar o spooler MAPI de que ele está em uma condição de erro grave. 
  
Para obter mais informações, [consulte Interagindo com o Spooler MAPI.](interacting-with-the-mapi-spooler.md) 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

