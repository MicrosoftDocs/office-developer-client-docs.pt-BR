---
title: Campos e itens do Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b40752d4a5f445368752ad4caf5c919f6e0ce27b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409115"
---
# <a name="outlook-items-and-fields"></a>Campos e itens do Outlook

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O Microsoft Outlook fornece tipos de item especializados para sua funcionalidade (por exemplo, itens de email, compromissos, contatos, tarefas e anotações). O Outlook fornece campos padrão para cada tipo de item, comumente chamados de campos internos. O Outlook também permite que os usuários criem campos personalizados, comumente chamados de campos definidos pelo usuário. Cada campo é associado a um tipo de dados e um valor. Exemplos de tipos de dados são **moeda**, **data/hora**, **duração**, **número inteiro**, **palavras-chave**e **texto**. Os usuários podem definir campos personalizados usando o designer de formulários no Outlook.
  
No nível de programação, cada item é representado por um objeto [IMessage](imessageimapiprop.md) . Cada campo definido pelo usuário é associado a uma definição de campo e um valor. 
  
### <a name="field-definition"></a>Definição de campo

Uma definição de campo inclui o nome, o tipo de dados e outras informações sobre o campo. Para cada item, o Outlook armazena as definições de todos os campos definidos pelo usuário na propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) do objeto **IMessage** correspondente. A propriedade **PidLidPropertyDefinitionStream** contém um fluxo binário conhecido como [PropertyDefinition](propertydefinition-stream-structure.md) que contém as definições de campo. Para obter mais informações sobre estruturas de fluxo para definições de campo, consulte [estruturas de fluxo](stream-structures.md).
  
### <a name="field-value"></a>Valor do campo

Cada campo definido pelo usuário de um item tem um valor que é armazenado em uma propriedade nomeada correspondente. Essa propriedade nomeada está no conjunto de propriedades PS_PUBLIC_STRINGS e tem uma cadeia de caracteres Unicode como o nome da propriedade. O tipo de dados da propriedade corresponde ao tipo do campo. Se a propriedade não estiver presente no objeto **IMessage** , o Outlook assumirá um valor padrão razoável para a propriedade. Por exemplo, para um tipo de cadeia de caracteres, o Outlook assume uma cadeia de caracteres vazia se a propriedade não estiver presente. 
  
## <a name="see-also"></a>Confira também



[Adicionar uma definição para um novo campo definido pelo usuário](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemplo de fluxo PropertyDefinition](propertydefinition-stream-sample.md)
  
[Estruturas de fluxo](stream-structures.md)
  
[Estrutura de fluxo PropertyDefinition](propertydefinition-stream-structure.md)
  
[Estrutura de fluxo FieldDefinition](fielddefinition-stream-structure.md)
  
[Estrutura de fluxo SkipBlock](skipblock-stream-structure.md)
  
[Estrutura de fluxo FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
  
[Estrutura de fluxo PackedAnsiString](packedansistring-stream-structure.md)
  
[Estrutura de fluxo PackedUnicodeString](packedunicodestring-stream-structure.md)

