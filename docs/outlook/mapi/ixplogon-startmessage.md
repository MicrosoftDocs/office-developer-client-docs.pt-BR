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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351594"
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
  
> no Serve deve ser zero.
    
 _lpMessage_
  
> no Um ponteiro para um objeto Message (representando a mensagem de entrada) que tem permissão de leitura/gravação, que é usada pelo provedor de transporte para acessar e manipular essa mensagem. Este objeto permanece válido até que o provedor de transporte retorne da chamada para **IXPLogon:: StartMessage**.
    
 _lpulMsgRef_
  
> bota Um ponteiro para um valor de referência atribuído à mensagem. O spooler MAPI inicializa esse valor como 1 antes de retornar o ponteiro para o provedor de transporte.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPLogon:: StartMessage** para iniciar a transferência de uma mensagem de entrada do provedor de transporte para o spooler MAPI. Antes de o provedor de transporte começar a usar a mensagem indicada pelo _lpMessage_, ele deve armazenar uma referência de mensagem no parâmetro _lpulMsgRef_ para uso potencial por uma chamada para o método [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) . 
  
Durante uma chamada **StartMessage** , o spooler MAPI processa os métodos para objetos abertos durante a transferência da mensagem e também processa qualquer anexo. Esse processamento pode levar muito tempo. Os provedores de transporte podem chamar a função de retorno de chamada [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) para o spooler MAPI com frequência durante esse processamento para liberar o tempo de CPU para outras tarefas do sistema. 
  
Todos os destinatários na tabela de destinatários que o provedor de transporte cria para a mensagem devem conter todas as propriedades de endereçamento necessárias. Se necessário, o provedor pode construir um destinatário personalizado para representar um determinado destinatário. No enTanto, se o provedor puder produzir uma entrada de destinatário que inclua mais informações, ele deverá fazer isso. Por exemplo, se um provedor de transporte tiver informações suficientes sobre o formato de destinatário de um provedor de catálogo de endereços que possa criar um identificador de entrada válido para um destinatário desse formato, ele deverá criar o identificador de entrada.
  
Se qualquer propriedade não-transmittable for recebida, o provedor de transporte não deverá armazená-las na nova mensagem. No enTanto, o provedor de transporte deve armazenar todas as propriedades de transmittable recebidas na nova mensagem.
  
Se a mensagem de entrada for um relatório de entrega ou um relatório de não entrega e o provedor de transporte não puder usar o método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) para gerar o relatório a partir da mensagem original, o provedor deverá preencher a mensagem com as propriedades adequadas. No enTanto, o provedor de transporte não pode definir a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da mensagem.
  
Para salvar a mensagem de entrada no repositório de mensagens MAPI apropriado após o processamento, o provedor de transporte chama o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Se o provedor de transporte não tiver nenhuma mensagem para passar para o spooler MAPI, ele poderá interromper a mensagem de entrada retornando da chamada **StartMessage** sem chamar **SaveChanges**.
  
Todos os objetos que o provedor de transporte abre durante uma chamada de **StartMessage** devem ser liberados antes de retornar. No enTanto, o provedor não deve liberar o objeto Message que o spooler MAPI aprovou originalmente no parâmetro _lpMessage_ . 
  
Se **StartMessage** retornar um erro, a mensagem em processo será lançada sem que as alterações sejam salvas e perdidas. Nesse caso, o provedor de transporte deve passar o sinalizador NOTIFY_CRITICAL_ERROR com uma chamada para o método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) e chamar o método [IXPLogon::P oll](ixplogon-poll.md) para NOTIFICAr o spooler MAPI de que ele está em uma condição de erro grave. 
  
Para obter mais informações, consulte [interagindo com o spooler MAPI](interacting-with-the-mapi-spooler.md). 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

