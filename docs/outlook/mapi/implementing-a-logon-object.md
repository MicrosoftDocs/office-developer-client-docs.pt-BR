---
title: Implementar um objeto de logon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e23c73931c9051b61d30b7ea7e9c54d06a4d9c33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767403"
---
# <a name="implementing-a-logon-object"></a>Implementar um objeto de logon

  
  
**Aplica-se a**: Outlook 
  
Cada catálogo de endereços, o armazenamento de mensagens e o provedor de transporte instancia um objeto de logon como parte de sua implementação do [IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)ou [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). Objetos de logon implementam métodos que ajudam a solicitações de cliente do serviço MAPI. Dependendo do tipo de provedor de serviços, seu objeto logon dará suporte a uma das seguintes interfaces. 
  
|**Interface de objeto de logon**|**Provedor de serviços**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Provedor de catálogo de endereços  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Provedor de armazenamento de mensagem  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Provedor de transporte  <br/> |
   
Mensagem e o catálogo de endereços armazenam provedores implementar os seguintes recursos nos seus objetos de logon:
  
- Suporte a notificação de evento (**Advise** e **Unadvise** métodos). Para obter uma visão geral da notificação de evento, consulte [A notificação de evento em MAPI](event-notification-in-mapi.md). Para obter mais informações sobre o suporte a notificação em seu objeto de logon, consulte [Suporte a notificação de evento](supporting-event-notification.md). 
    
- Comparação de identificador de entrada (método**CompareEntryIDs** ). Para obter informações gerais sobre identificadores de entrada, consulte [Identificadores de entrada de MAPI](mapi-entry-identifiers.md). Para obter mais informações sobre como comparar identificadores de entrada no método **CompareEntryIDs** do seu objeto logon, consulte [comparação e acesso a objetos com suporte](supporting-object-access-and-comparison.md).
    
- Acesso a informações de erro adicionais (método**GetLastError** ). Para obter mais informações sobre o tratamento de erros no MAPI, consulte o [Tratamento de erros no MAPI](error-handling-in-mapi.md). 
    
- Acesso aos objetos implementada pelo provedor de serviço (método**OpenEntry** ). Para obter mais informações, consulte [comparação e acesso a objetos com suporte](supporting-object-access-and-comparison.md).
    
- Acesso a um objeto de status (método**OpenStatusEntry** ). Para obter informações gerais sobre objetos de status, consulte [Objetos de Status de MAPI](mapi-status-objects.md). Para obter informações específicas sobre como implementar um objeto de status, consulte [Implementação do objeto de Status](status-object-implementation.md).
    
- Um processo de logoff (método**Logoff** ). Para obter mais informações, consulte [Sendo pressionada um provedor de serviços](shutting-down-a-service-provider.md).
    
Se seu provedor for um provedor de catálogo de endereços, você também implementar os seguintes métodos e os recursos associados:
  
- [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) para fornecer uma listagem dos modelos que você dá suporte para a criação de novos destinatários. Para obter mais informações, consulte [Tabelas únicos](one-off-tables.md) ou a [implementação de uma tabela únicos do provedor](implementing-a-provider-one-off-table.md).
    
- [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) para fornecer acesso à implementação de um destinatário cujos dados reside em um provedor de catálogo de endereço de host. Para obter mais informações, consulte [atuando como um provedor de catálogo de endereços estrangeira](acting-as-a-foreign-address-book-provider.md). 
    
- [IABLogon::PrepareRecips](iablogon-preparerecips.md) para garantir que as propriedades adequadas estão disponíveis para todos os destinatários em uma lista de destinatários. Para obter mais informações, consulte [IABLogon::PrepareRecips](iablogon-preparerecips.md). 
    
Objeto de logon de um provedor de transporte, que implementa [IXPLogon: IUnknown](ixplogoniunknown.md), é muito diferente do logon de objetos implementada por outros tipos de provedores de serviços. Ele possui apenas dois recursos em comum com os outros objetos de logon: acesso a um objeto de status por meio do método [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) e uma operação de logoff por meio do método [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) . Provedores de transporte implementam os seguintes recursos exclusivos de seus objetos de logon: 
  
- Registro para tipos de endereço (método[IXPLogon::AddressTypes](ixplogon-addresstypes.md) ). Para obter mais informações sobre como registrar um tipo de endereço, consulte o [provedor de transporte e o modelo operacional do Spooler de MAPI](transport-provider-and-mapi-spooler-operational-model.md).
    
- Controle de transmissão de mensagens (métodos[IXPLogon::StartMessage](ixplogon-startmessage.md), [IXPLogon::EndMessage](ixplogon-endmessage.md)e [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) ). Para obter mais informações, consulte [Modelo de recepção de mensagem](message-reception-model.md), [interagindo com o Spooler MAPI](interacting-with-the-mapi-spooler.md)e [Modelo de envio de mensagem](message-submission-model.md).
    
- Validação de estado interno (método[IXPLogon::ValidateState](ixplogon-validatestate.md) ). 
    
- Capacidade para baixar ou carregar mensagens por demanda (método[IXPLogon::FlushQueues](ixplogon-flushqueues.md) ). Para obter mais informações, consulte [Implementando o método FlushQueues](implementing-the-flushqueues-method.md).
    
- Capacidade para consultar mensagens (método[IXPLogon::Poll](ixplogon-poll.md) ) pendentes. Para obter mais informações, consulte [Modelo de recepção de mensagens](message-reception-model.md).
    
- Detecção de estado ocioso (método[IXPLogon::Idle](ixplogon-idle.md) ). 
    
- Interação com o MAPI spooler (método[IXPLogon::TransportNotify](ixplogon-transportnotify.md) ). 
    
## <a name="see-also"></a>Confira também



[Implementar o logon do provedor de serviços](implementing-service-provider-logon.md)

