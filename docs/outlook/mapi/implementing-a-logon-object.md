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
ms.openlocfilehash: f9d77313012c2d133dc9352707ebc5e0c69c9973
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332841"
---
# <a name="implementing-a-logon-object"></a>Implementar um objeto de logon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cada catálogo de endereços, repositório de mensagens e provedor de transporte cria uma instância de um objeto de logon como parte de sua implementação de [IABProvider:: logon](iabprovider-logon.md), [IMSProvider:: logon](imsprovider-logon.md)ou [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md). Os objetos de logon implementam métodos que ajudam solicitações de clientes de serviço MAPI. Dependendo do seu tipo de provedor de serviços, o objeto de logon dará suporte a uma das seguintes interfaces. 
  
|**Interface de objeto de logon**|**Provedor de serviços**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Provedor de catálogo de endereços  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Provedor de repositório de mensagens  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Provedor de transporte  <br/> |
   
Os provedores de catálogo de endereços e de repositório de mensagens implementam os seguintes recursos em seus objetos de logon:
  
- Suporte para notificação de eventos (métodos**Advise** e **Unadvise** ). Para obter uma visão geral da notificação de eventos, consulte [Event Notification in MAPI](event-notification-in-mapi.md). Para obter mais informações sobre a notificação de suporte em seu objeto de logon, consulte [support Event Notification](supporting-event-notification.md). 
    
- Comparação de identificador de entrada (método**CompareEntryIDs** ). Para obter informações gerais sobre identificadores de entrada, confira identificadores de [entrada MAPI](mapi-entry-identifiers.md). Para obter mais informações sobre a comparação de identificadores de entrada no método **CompareEntryIDs** do seu objeto de logon, consulte [support Object Access and Comparison](supporting-object-access-and-comparison.md).
    
- Acesso a informações de erro adicionais**** (método GetLastError). Para obter mais informações sobre o tratamento de erros no MAPI, consulte [tratamento de erros no MAPI](error-handling-in-mapi.md). 
    
- Acesso a objetos implementados pelo provedor de serviços (método**OpenEntry** ). Para obter mais informações, consulte [support Object Access and Comparison](supporting-object-access-and-comparison.md).
    
- Acesso a um objeto status (método**OpenStatusEntry** ). Para obter informações gerais sobre objetos de status, consulte [MAPI status Objects](mapi-status-objects.md). Para obter informações específicas sobre a implementação de um objeto status, consulte [status Object Implementation](status-object-implementation.md).
    
- Um processo de logoff (método de**logoff** ). Para obter mais informações, consulte desLigamento [de um provedor de serviços](shutting-down-a-service-provider.md).
    
Se seu provedor for um provedor de catálogo de endereços, você também implementará os seguintes métodos e recursos associados:
  
- [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) para fornecer uma lista dos modelos que você dá suporte à criação de novos destinatários. Para obter mais informações, consulte [tabelas de one-off](one-off-tables.md) ou [implementando uma tabela de um provedor](implementing-a-provider-one-off-table.md).
    
- [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) para fornecer acesso à implementação de um destinatário cujos dados residem em um provedor de catálogo de endereços de host. Para obter mais informações, consulte [atuando como um provedor de catálogo de endereços externo](acting-as-a-foreign-address-book-provider.md). 
    
- [IABLogon::P reparerecips](iablogon-preparerecips.md) para garantir que as propriedades apropriadas estejam disponíveis para todos os destinatários em uma lista de destinatários. Para obter mais informações, consulte [IABLogon::P reparerecips](iablogon-preparerecips.md). 
    
Um objeto de logon do provedor de transporte, que implementa [IXPLogon: IUnknown](ixplogoniunknown.md), é muito diferente dos objetos de logon implementados pelos outros tipos de provedores de serviço. Ele tem apenas dois recursos em comum com os outros objetos de logon: acesso a um objeto status através do método [IXPLogon:: OpenStatusEntry](ixplogon-openstatusentry.md) e uma operação de logoff por meio do método [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) . Os provedores de transporte implementam os seguintes recursos exclusivos em seus objetos de logon: 
  
- Registro para tipos de endereço (método[IXPLogon:: AddressTypes](ixplogon-addresstypes.md) ). Para obter mais informações sobre como registrar um tipo de endereço, consulte [Transport Provider and MAPI spooler operaTing Model](transport-provider-and-mapi-spooler-operational-model.md).
    
- Controle de transmissão de mensagem ([IXPLogon:: StartMessage](ixplogon-startmessage.md), [IXPLogon:: endmessage](ixplogon-endmessage.md)e [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) métodos). Para obter mais informações, consulte o [modelo de recebimento de mensagens](message-reception-model.md), interagindo [com o spooler MAPI e o](interacting-with-the-mapi-spooler.md)modelo de envio de [mensagens](message-submission-model.md).
    
- Validação de estado interno ([IXPLogon::](ixplogon-validatestate.md) método ValidateState). 
    
- Capacidade de baixar ou carregar mensagens sob demanda (método[IXPLogon:: FlushQueues](ixplogon-flushqueues.md) ). Para obter mais informações, consulte [implementar o método FlushQueues](implementing-the-flushqueues-method.md).
    
- Capacidade de consultar mensagens pendentes ([IXPLogon: método oll:P](ixplogon-poll.md) ). Para obter mais informações, consulte [Message recepções Model](message-reception-model.md).
    
- Detecção de estado ocioso ([IXPLogon:: método Idle](ixplogon-idle.md) ). 
    
- Interação com o spooler MAPI (método[IXPLogon:: TransportNotify](ixplogon-transportnotify.md) ). 
    
## <a name="see-also"></a>Confira também



[Implementar o logon do provedor de serviços](implementing-service-provider-logon.md)

