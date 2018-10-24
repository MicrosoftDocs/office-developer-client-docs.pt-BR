---
title: Adicionar uma definição de um novo campo definido pelo usuário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a2f9d1623c3733292ebf5c65452ac0d65f577c4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592714"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Adicionar uma definição de um novo campo definido pelo usuário
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

