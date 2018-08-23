---
title: Recursos opcionais para provedores do catálogo de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 378dcc3e1506432de22731a27731c58067647952
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565890"
---
# <a name="optional-features-for-address-book-providers"></a>Recursos opcionais para provedores do catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há muitos recursos opcionais para provedores de catálogo de endereços. Alguns dos recursos mais comumente implementados incluem:
  
- Atuando como um provedor estrangeiro permitindo entradas a partir de um dos seus contêineres a ser adicionado ao contêiner do outro provedor.
    
- Atuando como um provedor de host adicionando entradas a partir de outro provedor para um dos seus contêineres.
    
- Pesquisa avançada.
    
- Prefixo a rolagem por meio de tabelas de conteúdo.
    
- Suporte para listas de distribuição.
    
- Suporte a notificação de evento.
    
A tabela a seguir descreve brevemente esses recursos opcionais e como implementá-las:
  
|**Recurso**|**Como implementar**|
|:-----|:-----|
|Fornecer modelos para a criação de listas de destinatário de entradas para a mensagem  <br/> |Implemente o método [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) . Para obter mais informações, consulte [As tabelas de únicos](one-off-tables.md) e [Implementando únicos](implementing-one-off-tables.md).  <br/> |
|Destinatários do grupo em uma unidade nomeado  <br/> |Suporte para as propriedades de listas de distribuição por meio da implementação do [IDistList: IMAPIContainer](idistlistimapicontainer.md) interface.  <br/> |
|Atuar como um provedor de catálogo de endereço estrangeiro permitindo entradas a serem adicionadas a um recipiente em outro provedor  <br/> | Suporte para o código de vinculação de dados no provedor de host por:  <br/>  Dando suporte a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) em usuários e listas de distribuição de mensagens. Para obter mais informações, consulte [Identificadores de catálogo de endereços](address-book-identifiers.md).  <br/>  Implementando o método [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) . Para obter mais informações, consulte [atuando como um provedor de catálogo de endereços estrangeira](acting-as-a-foreign-address-book-provider.md).  <br/> |
|Atuando como um provedor de catálogo de endereço de host inserindo entradas de outro fornecedor  <br/> |Suporte para dados de vinculação para o código de um provedor estrangeiro chamando o método [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) . Para obter mais informações, consulte [atuando como um provedor de catálogo de endereço de Host](acting-as-a-host-address-book-provider.md).  <br/> |
|Prefixo de rolagem  <br/> |Suporte a restrições nas tabelas de conteúdo do contêiner. Para obter mais informações, consulte [Sobre restrições](about-restrictions.md).  <br/> |
|Em um contêiner de pesquisa avançada  <br/> |Suporte à propriedade **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) em contêineres. Para obter mais informações, consulte [Implementando a pesquisa avançada](implementing-advanced-searching.md).  <br/> |
|Notificação de evento  <br/> |Implemente os métodos [IABLogon::Advise](iablogon-advise.md) e [IABLogon::Unadvise](iablogon-unadvise.md) . Para obter mais informações, consulte [A notificação de evento em MAPI](event-notification-in-mapi.md) e [Suporte a notificação de evento](supporting-event-notification.md).  <br/> |
   
Para fins de notificação de evento, o método **IABLogon::Advise** será chamado pelo MAPI quando um cliente chama **IAddrBook::Advise** para registrar para notificações de qualquer um dos seus contêineres, usuários ou listas de distribuição de mensagens. No entanto, como notificação de evento de suporte é opcional, você pode retornar MAPI_E_NO_SUPPORT entre esses métodos. No entanto, MAPI recomendável pelo menos suporte a notificações de suas tabelas de conteúdo e incentiva a oferecer suporte a todos os tipos de notificação de objeto, exceto _fnevSearchComplete_ e o evento _fnevCriticalError_ para adicionar valor. 
  

