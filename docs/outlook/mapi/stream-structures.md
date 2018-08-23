---
title: Estruturas de fluxo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5f372e93457f2b7ef8830ae6bd0363f6b3a7bd60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581577"
---
# <a name="stream-structures"></a>Estruturas de fluxo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Definições de campos definida pelo usuário de um item do Microsoft Outlook são armazenadas na propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) . O valor dessa propriedade é um fluxo binário que contém definições de campos definidos pelo usuário e configurações de associação de dados para campos internos do item do Outlook. Esta seção fornece informações sobre a estrutura do fluxo binário, decomposta nas seguintes estruturas stream. 
  
> [!NOTE]
> Os nomes dessas estruturas stream (por exemplo, PropertyDefinition, FieldDefinition e SkipBlock) e seus elementos de dados não são tecnicamente fazem parte da interface de programação de API do MAPI (Messaging) e são oferecidos apenas para documentação fins as estruturas de fluxo real. Desenvolvedores podem rotular esses elementos de estruturas e os dados de fluxo em seus aplicativos de forma que preferirem. 
  
- [Estrutura de fluxo de PropertyDefinition](propertydefinition-stream-structure.md)
    
- [Estrutura de fluxo de FieldDefinition](fielddefinition-stream-structure.md)
    
- [Estrutura de fluxo de SkipBlock](skipblock-stream-structure.md)
    
- [Estrutura de fluxo de FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [Estrutura de fluxo de PackedAnsiString](packedansistring-stream-structure.md)
    
- [Estrutura de fluxo de PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Confira também



[Campos e itens do Outlook](outlook-items-and-fields.md)
  
[Adicionar uma definição de um novo campo definido pelo usuário](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemplo de fluxo de PropertyDefinition](propertydefinition-stream-sample.md)

