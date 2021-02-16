---
title: Estruturas de fluxo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407820"
---
# <a name="stream-structures"></a>Estruturas de fluxo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As definições de campos definidos pelo usuário de um item do Microsoft Outlook são armazenadas na propriedade [PidLidPropertyDefinitionStream.](pidlidpropertydefinitionstream-canonical-property.md) O valor dessa propriedade é um fluxo binário que contém definições de campos definidos pelo usuário e configurações de vinculação de dados para campos integrados para o item do Outlook. Esta seção fornece informações sobre a estrutura do fluxo binário, dividida nas estruturas de fluxo a seguir. 
  
> [!NOTE]
> Os nomes dessas estruturas de fluxo (por exemplo, PropertyDefinition, FieldDefinition e SkipBlock) e seus elementos de dados não fazem parte tecnicamente da interface de programação da API de Mensagens (MAPI) e são fornecidos aqui apenas para fins de documentação das estruturas de fluxo reais. Os desenvolvedores podem rotular essas estruturas de fluxo e elementos de dados em seus aplicativos conforme eles escolherem. 
  
- [Estrutura de fluxo PropertyDefinition](propertydefinition-stream-structure.md)
    
- [Estrutura de Fluxo de FieldDefinition](fielddefinition-stream-structure.md)
    
- [Estrutura de fluxo SkipBlock](skipblock-stream-structure.md)
    
- [Estrutura de fluxo firstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [Estrutura de fluxo de PackedAnsiString](packedansistring-stream-structure.md)
    
- [Estrutura de fluxo de PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Confira também



[Campos e itens do Outlook](outlook-items-and-fields.md)
  
[Adicionar uma definição para um novo User-Defined campo](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemplo de fluxo propertyDefinition](propertydefinition-stream-sample.md)

