---
title: Recursos opcionais para provedores de catálogo de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9f5d8f0cd1b21f58e4e5c7d7ccd6cb19f3626c38
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414568"
---
# <a name="optional-features-for-address-book-providers"></a>Recursos opcionais para provedores de catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há vários recursos opcionais para provedores de catálogo de endereços. Alguns dos recursos mais comumente implementados incluem:
  
- Atuar como um provedor externo, permitindo que entradas de um dos seus contêineres sejam adicionados ao contêiner de outro provedor.
    
- Atuar como um provedor de host adicionando entradas de outro provedor a um dos seus contêineres.
    
- Pesquisa avançada.
    
- Prefixo rolando pelas tabelas de conteúdo.
    
- Suporte para listas de distribuição.
    
- Suporte para notificação de eventos.
    
A tabela a seguir descreve brevemente estes recursos opcionais e como implementá-los:
  
|**Recurso**|**Como implementar**|
|:-----|:-----|
|Fornecer modelos para criar entradas para listas de destinatários de mensagens  <br/> |Implemente o método [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) . Para obter mais informações, consulte [tabelas de one-off](one-off-tables.md) e [implementando tabelas individuais](implementing-one-off-tables.md).  <br/> |
|Agrupar destinatários em uma unidade nomeada  <br/> |Dê suporte às propriedades de listas de distribuição implementando a interface [IDistList: IMAPIContainer](idistlistimapicontainer.md) .  <br/> |
|Atuar como um provedor de catálogo de endereços externo, permitindo que entradas sejam adicionadas a um contêiner em outro provedor  <br/> | Dê suporte à associação de código aos dados no provedor de host por:  <br/>  Suporte à propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) em usuários de mensagens e listas de distribuição. Para obter mais informações, consulte Identificadores do [Catálogo de endereços](address-book-identifiers.md).  <br/>  Implementar o método [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) . Para obter mais informações, consulte [atuando como um provedor de catálogo de endereços externo](acting-as-a-foreign-address-book-provider.md).  <br/> |
|Atuar como um provedor de catálogo de endereços de host inserindo entradas de outro provedor  <br/> |Dê suporte à vinculação de dados ao código de um provedor estrangeiro chamando o método [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) . Para obter mais informações, consulte [atuando como um provedor de catálogo de endereços de host](acting-as-a-host-address-book-provider.md).  <br/> |
|Rolagem de prefixo  <br/> |Restrições de suporte nas tabelas de conteúdo do contêiner. Para obter mais informações, consulte [about Restrictions](about-restrictions.md).  <br/> |
|Pesquisa avançada em um contêiner  <br/> |Suporta a propriedade **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) em contêineres. Para obter mais informações, consulte [implementação de pesquisa avançada](implementing-advanced-searching.md).  <br/> |
|Notificação de eventos  <br/> |Implemente os métodos [IABLogon:: Advise](iablogon-advise.md) e [IABLogon:: Unadvise](iablogon-unadvise.md) . Para obter mais informações, consulte [Event Notification in MAPI](event-notification-in-mapi.md) and [support Event Notification](supporting-event-notification.md).  <br/> |
   
Para notificação de eventos, o método **IABLogon:: Advise** será chamado por MAPI quando um cliente chama **IAddrBook:: Advise** para registrar notificações em qualquer um dos seus contêineres, usuários de mensagens ou listas de distribuição. No enTanto, como a notificação de evento de suporte é opcional, você pode retornar MAPI_E_NO_SUPPORT desses métodos. No enTanto, o MAPI recomenda que você tenha pelo menos notificações de suporte em suas tabelas de conteúdo e o incentiva a oferecer suporte a todos os tipos de notificação de objeto, exceto _fnevSearchComplete_ e o evento _fnevCriticalError_ para adicionar valor. 
  

