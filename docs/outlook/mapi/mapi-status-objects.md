---
title: Objetos de status MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 816d1b7c9c0b8c5a80a2351580ce3224fccf0b14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406742"
---
# <a name="mapi-status-objects"></a>Objetos de status MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os objetos de status relatam informações sobre recursos MAPI. Por exemplo, um provedor de serviços, o processo de envio/recebimento de MAPI ou o catálogo de endereços.
  
Há um objeto de status fornecendo informações sobre cada provedor de serviços individual no perfil atual. O MAPI é responsável pela implementação de objetos de status para o subsistema, o processo de envio/recebimento de MAPI e o catálogo de endereços. O objeto de status do subsistema fornece informações globais. O objeto status do catálogo de endereços integrado fornece o status de todos os provedores de catálogo de endereços operando no momento.
  
Cada objeto de status é incluído na tabela de status, uma tabela mantida por MAPI que fornece aos clientes todas as informações de status da sessão. Para obter mais informações, consulte [tabelas de status](status-tables.md). Os clientes podem acessar um determinado objeto status através da tabela ou, para um provedor de serviços, por meio do objeto de logon. Por exemplo, para acessar um objeto status do provedor de catálogo de endereços, um cliente pode chamar **IABLogon:: OpenStatusEntry**. Para obter mais informações, consulte [IABLogon:: OpenStatusEntry](iablogon-openstatusentry.md).
  
Os clientes podem usar os objetos de status para:
  
- Saiba mais sobre o estado de uma sessão.
    
- Monitorar um provedor de serviços.
    
- Controlar a transmissão de mensagens.
    
- Exibir ou alterar a configuração e o status de um recurso.
    
Cada objeto de status implementa a interface **IMAPIStatus** . Para obter mais informações, consulte [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md). No enTanto, nem todos os objetos de status oferecem suporte total a todos os métodos **IMAPIStatus** . Como há variação nos métodos que são suportados por um objeto status, os clientes precisam aprender sobre um determinado objeto status antes de poderem usá-lo. Os objetos de status são necessários para publicar informações sobre seus recursos nas três propriedades a seguir: 
  
 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
Para obter mais informações sobre a implementação de um objeto status, consulte [status Object Implementation](status-object-implementation.md). Para obter mais informações sobre como usar um objeto status, consulte [tabela de status e objetos de status](status-table-and-status-objects.md).
  

