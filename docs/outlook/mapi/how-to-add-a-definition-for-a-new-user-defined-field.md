---
title: Adicionar uma definição de um novo campo definido pelo usuário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428162"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Adicionar uma definição de um novo campo definido pelo usuário
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao adicionar um campo definido pelo usuário a um item do Microsoft Outlook, você adiciona uma definição de campo à estrutura de fluxo [PropertyDefinition](propertydefinition-stream-structure.md) correspondente. Use o procedimento a seguir para adicionar uma nova definição de campo a uma estrutura de fluxo PropertyDefinition. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>Para adicionar uma definição para um novo campo definido pelo usuário

1. Copie as definições de campo existentes da estrutura de fluxo PropertyDefinition para uma nova matriz de definições de campo. 
    
2. Se alguma definição de campo existente estiver no formato PropDefV1, converta-as no formato PropDefV2. Para obter mais informações sobre formatos de definição de campo, consulte [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) e [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).
    
3. Crie uma definição do novo campo definido pelo usuário no formato PropDefV2 e adicione-o à matriz.
    
4. Defina o elemento Version da estrutura de fluxo PropertyDefinition como 0x0103, se o elemento Version não tiver sido definido com esse valor.
    
5. Incremente o elemento FieldDefinitionCount em 1.
    
6. Armazene a matriz como o valor do elemento FieldDefinitions.
    
## <a name="see-also"></a>Confira também

- [Estrutura de fluxo PropertyDefinition](propertydefinition-stream-structure.md)

