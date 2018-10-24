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
ms.openlocfilehash: 0366e889f1c63e5fe40760ca80cec701cd6b3713
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573534"
---
# <a name="opening-the-default-message-store"></a>Abrir um repositório de mensagens padrão

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Em qualquer sessão específica, um armazenamento de mensagens atua como o armazenamento de mensagens padrão. Um armazenamento de mensagens padrão tem as seguintes características:
  
- A propriedade **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) é definida como TRUE.
    
- O sinalizador STATUS_DEFAULT_STORE é definido na propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- MAPI cria automaticamente a subárvore IPM e as pastas raiz para resultados de pesquisa, modos de exibição comuns e exibições pessoais quando o armazenamento de mensagens é aberto. Para obter mais informações sobre essas pastas, consulte [Subárvore IPM](ipm-subtree.md) e [Pastas especiais de MAPI](mapi-special-folders.md). 
    
Para recuperar o identificador de entrada para o armazenamento de mensagens padrão, você deve chamar [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir a tabela de repositório de mensagens e aplicar uma restrição apropriada em uma chamada para [HrQueryAllRows](hrqueryallrows.md). **HrQueryAllRows** retornará uma linha definidas com uma linha que representa o armazenamento de mensagens padrão. A restrição que você passa para **HrQueryAllRows** pode ser realizadas em um dos seguintes formatos: 
  
1. Uma restrição **e** que usa uma estrutura de **SAndRestriction** para combinar: 
    
   - Uma restrição que usa uma estrutura de **SExistRestriction** para testar a existência da propriedade **PR_DEFAULT_STORE** de existir. 
    
   - Uma restrição de propriedade que usa uma estrutura de [SPropertyRestriction](spropertyrestriction.md) para verificar o valor TRUE na propriedade **PR_DEFAULT_STORE** . 
    
2. Uma restrição de bitmask que usa uma estrutura de [SBitMaskRestriction](sbitmaskrestriction.md) para a aplicação de STATUS_DEFAULT_STORE como uma máscara contra a propriedade **PR_RESOURCE_FLAGS** . 
    
## <a name="see-also"></a>Confira também

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

