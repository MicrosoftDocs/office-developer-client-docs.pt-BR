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
  
Em qualquer sessão específica, um repositório de mensagens atua como o repositório de mensagens padrão. Um repositório de mensagens padrão tem as seguintes características:
  
- A propriedade **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) é definida como true.
    
- O sinalizador STATUS_DEFAULT_STORE é definido na propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- O MAPI cria automaticamente a subárvore IPM e as pastas raiz para resultados de pesquisa, modos de exibição e modos de exibição pessoais quando o repositório de mensagens é aberto. Para obter mais informações sobre essas pastas, consulte [IPM sub-árvore](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md). 
    
Para recuperar o identificador de entrada para o repositório de mensagens padrão, você deve chamar [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir a tabela de repositório de mensagens e aplicar uma restrição apropriada em uma chamada para [HrQueryAllRows](hrqueryallrows.md). **HrQueryAllRows** retornará um conjunto de linhas com uma linha que representa o repositório de mensagens padrão. A restrição que você passa para o **HrQueryAllRows** pode executar um dos seguintes formatos: 
  
1. Uma restrição **e** que usa uma estrutura **SAndRestriction** para combinar: 
    
   - Uma restrição Exists que usa uma estrutura **SExistRestriction** para testar a existência da propriedade **PR_DEFAULT_STORE** . 
    
   - Uma restrição de propriedade que usa uma estrutura [SPropertyRestriction](spropertyrestriction.md) para verificar o valor true na propriedade **PR_DEFAULT_STORE** . 
    
2. Uma restrição de bitmask que usa uma estrutura [SBitMaskRestriction](sbitmaskrestriction.md) para aplicar STATUS_DEFAULT_STORE como uma máscara à propriedade **PR_RESOURCE_FLAGS** . 
    
## <a name="see-also"></a>Confira também

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

