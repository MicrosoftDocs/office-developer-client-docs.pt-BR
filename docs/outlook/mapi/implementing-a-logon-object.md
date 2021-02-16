---
title: Implementando um objeto logon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f9d77313012c2d133dc9352707ebc5e0c69c9973
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433042"
---
# <a name="implementing-a-logon-object"></a>Implementando um objeto logon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cada livro de endereços, armazenamento de mensagens e provedor de transporte instanam um objeto de logon como parte de sua implementação de [IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)ou [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). Os objetos de logon implementam métodos que ajudam as solicitações do cliente de serviço MAPI. Dependendo do tipo de provedor de serviços, o objeto de logon dará suporte a uma das interfaces a seguir. 
  
|**Interface de objeto de logon**|**Provedor de serviços**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Provedor de agendas  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Provedor de armazenamento de mensagens  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Provedor de transporte  <br/> |
   
Os provedores de armazenamento de mensagens e de agenda de endereço implementam os seguintes recursos em seus objetos de logon:
  
- Suporte para notificação de evento (**métodos Advise** e **Unadvise).** Para uma visão geral da notificação de evento, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md). Para obter mais informações sobre o suporte à notificação no objeto de logon, consulte [Notificação de Evento de Suporte.](supporting-event-notification.md) 
    
- Comparação do identificador de entrada **(método CompareEntryIDs).** Para obter informações gerais sobre identificadores de entrada, consulte [MapI Entry Identifiers](mapi-entry-identifiers.md). Para obter mais informações sobre como comparar identificadores de entrada no método **CompareEntryIDs** do objeto de logon, consulte Suporte ao acesso a objetos [e comparação.](supporting-object-access-and-comparison.md)
    
- Acesso a informações de erro adicionais **(método GetLastError).** For more information about handling errors in MAPI, see [Error Handling in MAPI](error-handling-in-mapi.md). 
    
- Acesso a objetos implementados pelo provedor de serviços **(método OpenEntry).** Para obter mais informações, consulte [Suporte ao acesso e comparação de objetos.](supporting-object-access-and-comparison.md)
    
- Acesso a um objeto de status **(método OpenStatusEntry).** Para obter informações gerais sobre objetos de status, consulte [MAPI Status Objects](mapi-status-objects.md). Para obter informações específicas sobre a implementação de um objeto de status, consulte [Implementação de objeto de status.](status-object-implementation.md)
    
- Um processo de logoff **(método Logoff).** Para obter mais informações, [consulte Desligar um Provedor de Serviços.](shutting-down-a-service-provider.md)
    
Se o provedor for um provedor de agendas de endereços, você também implementará os seguintes métodos e recursos associados:
  
- [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) para fornecer uma listagem dos modelos com suporte para a criação de novos destinatários. Para obter mais informações, [consulte Tabelas One-Off](one-off-tables.md) ou [Implementando um provedor One-Off tabela](implementing-a-provider-one-off-table.md).
    
- [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) para fornecer acesso à implementação de um destinatário cujos dados residem em um provedor de agendamento de endereço de host. Para obter mais informações, consulte [Agindo como um provedor de livros de endereços externos.](acting-as-a-foreign-address-book-provider.md) 
    
- [IABLogon::P repareRecips](iablogon-preparerecips.md) para garantir que as propriedades apropriadas estão disponíveis para todos os destinatários em uma lista de destinatários. Para obter mais informações, [consulte IABLogon::P repareRecips](iablogon-preparerecips.md). 
    
Um objeto de logon do provedor de transporte, que implementa [IXPLogon : IUnknown](ixplogoniunknown.md), é bem diferente dos objetos de logon implementados pelos outros tipos de provedores de serviços. Ele tem apenas dois recursos em comum com os outros objetos de logon: acesso a um objeto de status por meio do método [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) e uma operação de logoff por meio do método [IXPLogon::TransportLogoff.](ixplogon-transportlogoff.md) Os provedores de transporte implementam os seguintes recursos exclusivos em seus objetos de logon: 
  
- Registro para tipos de endereço ([método IXPLogon::AddressTypes).](ixplogon-addresstypes.md) Para obter mais informações sobre como registrar um tipo de endereço, consulte o Provedor de Transporte e o Modelo [Operacional do Spooler MAPI.](transport-provider-and-mapi-spooler-operational-model.md)
    
- Controle da transmissão de mensagens ([métodos IXPLogon::StartMessage](ixplogon-startmessage.md), [IXPLogon::EndMessage](ixplogon-endmessage.md)e [IXPLogon::SubmitMessage).](ixplogon-submitmessage.md) Para obter mais informações, consulte [Modelo de recepção de](message-reception-model.md)mensagens , interagindo com o [Spooler MAPI](interacting-with-the-mapi-spooler.md)e o modelo de envio [de mensagem](message-submission-model.md).
    
- Validação de estado interno[(método IXPLogon::ValidateState).](ixplogon-validatestate.md) 
    
- Capacidade de baixar ou carregar mensagens sob demanda ([método IXPLogon::FlushQueues).](ixplogon-flushqueues.md) Para obter mais informações, [consulte Implementando o método FlushQueues](implementing-the-flushqueues-method.md).
    
- Capacidade de consultar mensagens pendentes[(método IXPLogon::P oll).](ixplogon-poll.md) Para obter mais informações, consulte [o Modelo de Recepção de Mensagens.](message-reception-model.md)
    
- Detecção de estado ocioso[(método IXPLogon::Idle).](ixplogon-idle.md) 
    
- Interação com o spooler MAPI ([método IXPLogon::TransportNotify).](ixplogon-transportnotify.md) 
    
## <a name="see-also"></a>Confira também



[Implementando o logon do provedor de serviços](implementing-service-provider-logon.md)

