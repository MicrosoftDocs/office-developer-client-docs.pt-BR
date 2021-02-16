---
title: Recursos opcionais para provedores de lista de endereços
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
# <a name="optional-features-for-address-book-providers"></a>Recursos opcionais para provedores de lista de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há muitos recursos opcionais para provedores de agendas. Alguns dos recursos mais comumente implementados incluem:
  
- Atuar como um provedor estrangeiro, permitindo que entradas de um de seus contêineres sejam adicionadas ao contêiner de outro provedor.
    
- Atuar como um provedor de host adicionando entradas de outro provedor a um de seus contêineres.
    
- Pesquisa avançada.
    
- Prefixo rolando pelas tabelas de conteúdo.
    
- Suporte para listas de distribuição.
    
- Suporte para notificação de evento.
    
A tabela a seguir descreve brevemente esses recursos opcionais e como implementá-los:
  
|**Característica**|**Como implementar**|
|:-----|:-----|
|Modelos de fornecimento para a criação de entradas para listas de destinatários de mensagens  <br/> |Implemente [o método IABLogon::GetOneOffTable.](iablogon-getoneofftable.md) Para obter mais informações, consulte [Tabelas One-Off](one-off-tables.md) e [Implementando One-Off Tabelas.](implementing-one-off-tables.md)  <br/> |
|Agrupar destinatários em uma unidade nomeada  <br/> |Suporte às propriedades das listas de distribuição implementando a interface [IDistList : IMAPIContainer.](idistlistimapicontainer.md)  <br/> |
|Atuar como um provedor de agendamento externo, permitindo que entradas sejam adicionadas a um contêiner em outro provedor  <br/> | Suporte ao código de associação aos dados no provedor de host ao:  <br/>  Suporte à **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) em usuários de mensagens e listas de distribuição. Para obter mais informações, consulte [Identificadores do Livro de Endereços.](address-book-identifiers.md)  <br/>  Implementando o [método IABLogon::OpenTemplateID.](iablogon-opentemplateid.md) Para obter mais informações, [consulte Agindo como um provedor de livros de endereços externos.](acting-as-a-foreign-address-book-provider.md)  <br/> |
|Agindo como um provedor de agendamento de host inserindo entradas de outro provedor  <br/> |Suporte à vinculação de dados ao código de um provedor estrangeiro chamando o [método IMAPISupport::OpenTemplateID.](imapisupport-opentemplateid.md) Para obter mais informações, consulte [Agindo como um provedor de agenda de endereços de host.](acting-as-a-host-address-book-provider.md)  <br/> |
|Rolagem de prefixo  <br/> |Restrições de suporte em tabelas de conteúdo do contêiner. Para obter mais informações, consulte [Sobre restrições.](about-restrictions.md)  <br/> |
|Pesquisa avançada em um contêiner  <br/> |Suporte à **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) em contêineres. Para obter mais informações, [consulte Implementando a Pesquisa Avançada.](implementing-advanced-searching.md)  <br/> |
|Notificação de evento  <br/> |Implemente [os métodos IABLogon::Advise](iablogon-advise.md) e [IABLogon::Unadvise.](iablogon-unadvise.md) Para obter mais informações, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md) e [notificação de evento de suporte.](supporting-event-notification.md)  <br/> |
   
Para notificação de evento, seu método **IABLogon::Advise** será chamado pelo MAPI quando um cliente chamar **IAddrBook::Advise** para registrar-se para notificações em qualquer um dos seus contêineres, usuários de mensagens ou listas de distribuição. No entanto, como a notificação de evento de suporte é opcional, você pode retornar MAPI_E_NO_SUPPORT desses métodos. No entanto, o MAPI recomenda que você pelo menos suporte notificações em suas tabelas de conteúdo e incentiva você a dar suporte a todos os tipos de notificação de objeto, exceto  _para fnevSearchComplete_ e o evento  _fnevCriticalError_ para adicionar valor. 
  

