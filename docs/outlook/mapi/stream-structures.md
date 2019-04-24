---
title: Estruturas de fluxo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327437"
---
# <a name="stream-structures"></a>Estruturas de fluxo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Definições de campos definidos pelo usuário de um item do Microsoft Outlook são armazenadas na propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) . O valor dessa propriedade é um fluxo binário que contém definições de campos definidos pelo usuário e configurações de associação de dados para campos internos para o item do Outlook. Esta seção fornece informações sobre a estrutura do fluxo binário, divididas nas estruturas de fluxo a seguir. 
  
> [!NOTE]
> Os nomes dessas estruturas de fluxo (por exemplo, PropertyDefinition, FieldDefinition e SkipBlock) e seus elementos de dados não são tecnicamente parte da interface de programação da API de mensagens (MAPI) e são fornecidos aqui somente para documentação objetivos das estruturas de fluxo reais. Os desenvolvedores podem rotular essas estruturas de fluxo e elementos de dados em seus aplicativos, conforme eles escolhem. 
  
- [Estrutura de fluxo PropertyDefinition](propertydefinition-stream-structure.md)
    
- [Estrutura de fluxo FieldDefinition](fielddefinition-stream-structure.md)
    
- [Estrutura de fluxo SkipBlock](skipblock-stream-structure.md)
    
- [Estrutura de fluxo FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [Estrutura de fluxo PackedAnsiString](packedansistring-stream-structure.md)
    
- [Estrutura de fluxo PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Confira também



[Campos e itens do Outlook](outlook-items-and-fields.md)
  
[Adicionar uma definição para um novo campo definido pelo usuário](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemplo de fluxo PropertyDefinition](propertydefinition-stream-sample.md)

