---
title: Adicione uma definição para um novo campo definido pelo usuário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 26c329323eebff6cfdf4f4be4dffe9a62f8745e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766703"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Adicione uma definição para um novo campo definido pelo usuário
 
**Aplica-se a**: Outlook 
  
Quando você adiciona um campo definido pelo usuário a um item do Microsoft Outlook, você adicionar uma definição de campo na estrutura do stream [PropertyDefinition](propertydefinition-stream-structure.md) correspondente. Use o procedimento a seguir para adicionar uma nova definição de campo para uma estrutura de fluxo de PropertyDefinition. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>Para adicionar uma definição para um novo campo definido pelo usuário

1. Copie as definições de campo existentes da estrutura PropertyDefinition stream para uma nova matriz de definições de campo. 
    
2. Se quaisquer definições de campo existente no formato PropDefV1, convertê-los para o formato de PropDefV2. Para obter mais informações sobre formatos de definição de campo, consulte [PropertyDefinition Stream](propertydefinition-stream-structure.md) e [Estrutura do fluxo de FieldDefinition](fielddefinition-stream-structure.md).
    
3. Criar uma definição do novo campo definido pelo usuário no formato PropDefV2 e adicioná-lo à matriz.
    
4. Defina o elemento de versão da estrutura PropertyDefinition stream como 0x0103, se o elemento de versão não tiver sido definido para esse valor.
    
5. Aumentam o elemento FieldDefinitionCount em 1.
    
6. Armazene a matriz como o valor do elemento FieldDefinitions.
    
## <a name="see-also"></a>Confira também

- [Estrutura de fluxo de PropertyDefinition](propertydefinition-stream-structure.md)

