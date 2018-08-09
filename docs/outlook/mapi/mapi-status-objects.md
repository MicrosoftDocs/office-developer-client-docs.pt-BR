---
title: Objetos de Status MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f5b48f8cd4ef6ff41733ec9a18d1ab682f5e6bcb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767963"
---
# <a name="mapi-status-objects"></a>Objetos de Status MAPI

  
  
**Aplica-se a**: Outlook 
  
Objetos de status relatar informações sobre os recursos MAPI. Por exemplo, um provedor de serviços, o processo de envio/recebimento de MAPI ou o catálogo de endereços.
  
Não há um objeto de status, fornecendo informações sobre cada provedor de serviços individuais no perfil atual. MAPI é responsável por implementar objetos de status para o catálogo de endereços, o processo de envio/recebimento de MAPI e o subsistema. O objeto de status do subsistema fornece informações globais. O objeto de status para o catálogo de endereços integrada fornece o status de todos os provedores de catálogo de endereços funcionando no momento.
  
Cada objeto de status é incluído na tabela de status, na tabela mantida pelo MAPI que fornece aos clientes com todas as informações de status para a sessão. Para obter mais informações, consulte as [Tabelas de Status](status-tables.md). Clientes podem acessar um objeto de status específico por meio da tabela ou, para um provedor de serviço, por meio de seu objeto de logon. Por exemplo, para acessar o objeto de status de um provedor catálogo de endereços, um cliente pode chamar **IABLogon::OpenStatusEntry**. Para obter mais informações, consulte [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).
  
Os clientes podem usar os objetos de status para:
  
- Saiba mais sobre o estado da sessão.
    
- Monitore a um provedor de serviços.
    
- Controle de transmissão da mensagem.
    
- Exibir ou alterar a configuração e o status do recurso.
    
Cada objeto de status implementa a interface de **IMAPIStatus** . Para obter mais informações, consulte [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md). No entanto, não a cada objeto de status totalmente fornece suporte a cada método **IMAPIStatus** . Como há variação nos métodos suportados por um objeto de status, os clientes precisam aprender sobre um objeto determinado status antes que eles podem usá-lo. Objetos de status são necessários para publicar informações sobre seus recursos nas seguintes três propriedades: 
  
 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
Para obter mais informações sobre como implementar um objeto de status, consulte o [Status de implementação de objeto](status-object-implementation.md). Para obter mais informações sobre como usar um objeto de status, consulte a [tabela de Status e objetos de Status](status-table-and-status-objects.md).
  

