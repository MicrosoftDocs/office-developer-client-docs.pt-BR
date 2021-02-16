---
title: Abrir um repositório de mensagens padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d8e620516e2b3e61cd07f3a08af989cc4ed5b61e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436024"
---
# <a name="opening-the-default-message-store"></a>Abrir um repositório de mensagens padrão

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Em qualquer sessão específica, um armazenamento de mensagens atua como o armazenamento de mensagens padrão. Um armazenamento de mensagens padrão tem as seguintes características:
  
- A **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) é definida como TRUE.
    
- O STATUS_DEFAULT_STORE sinalizador é definido **na propriedade PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened. Para obter mais informações sobre essas pastas, consulte [Subárvore IPM](ipm-subtree.md) e [Pastas Especiais MAPI.](mapi-special-folders.md) 
    
Para recuperar o identificador de entrada para o armazenamento de mensagens padrão, você deve chamar [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir a tabela de armazenamento de mensagens e aplicar uma restrição apropriada em uma chamada para [HrQueryAllRows](hrqueryallrows.md). **HrQueryAllRows** retornará um conjunto de linhas com a única linha que representa o armazenamento de mensagens padrão. A restrição que você passa **para HrQueryAllRows** pode assumir em um dos seguintes formulários: 
  
1. Uma **restrição AND** que usa uma **estrutura SAndRestriction** para combinar: 
    
   - Existe uma restrição que usa **uma estrutura SExistRestriction** para testar a existência da **PR_DEFAULT_STORE** propriedade. 
    
   - Uma restrição de propriedade que usa uma [estrutura SPropertyRestriction](spropertyrestriction.md) para verificar o valor TRUE na **PR_DEFAULT_STORE** propriedade. 
    
2. Uma restrição de bitmask que usa uma estrutura [SBitMaskRestriction](sbitmaskrestriction.md) para aplicar STATUS_DEFAULT_STORE como uma máscara contra a **PR_RESOURCE_FLAGS** propriedade. 
    
## <a name="see-also"></a>Confira também

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

