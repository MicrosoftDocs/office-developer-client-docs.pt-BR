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
  
Os objetos de status relatam informações sobre recursos MAPI. Por exemplo, um provedor de serviços, o processo de envio/recebimento MAPI ou o livro de endereços.
  
Há um objeto de status que fornece informações sobre cada provedor de serviços individual no perfil atual. MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book. O objeto de status do subsistema fornece informações globais. O objeto de status do livro de endereços integrado fornece o status de todos os provedores de agendas que operam no momento.
  
Cada objeto de status é incluído na tabela de status, uma tabela mantida pela MAPI que fornece aos clientes todas as informações de status da sessão. Para obter mais informações, consulte [Tabelas de Status.](status-tables.md) Os clientes podem acessar um objeto de status específico por meio da tabela ou, para um provedor de serviços, por meio de seu objeto de logon. Por exemplo, para acessar o objeto de status de um provedor de agendamento de endereços, um cliente pode chamar **IABLogon::OpenStatusEntry**. Para obter mais informações, consulte [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).
  
Os clientes podem usar objetos de status para:
  
- Saiba mais sobre o estado de uma sessão.
    
- Monitore um provedor de serviços.
    
- Controlar a transmissão de mensagens.
    
- Exibir ou alterar a configuração e o status de um recurso.
    
Cada objeto de status implementa a interface **IMAPIStatus.** Para obter mais informações, [consulte IMAPIStatus : IMAPIProp](imapistatusimapiprop.md). No entanto, nem todos os objetos de status são compatíveis com todos **os métodos IMAPIStatus.** Como há variação nos métodos suportados por um objeto de status, os clientes precisam aprender sobre um objeto de status específico antes de poder usá-lo. Os objetos de status são necessários para publicar informações sobre seus recursos nas três propriedades a seguir: 
  
 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
Para obter mais informações sobre a implementação de um objeto de status, consulte [Implementação de objeto de status.](status-object-implementation.md) Para obter mais informações sobre como usar um objeto de status, consulte [Status Table and Status Objects](status-table-and-status-objects.md).
  

