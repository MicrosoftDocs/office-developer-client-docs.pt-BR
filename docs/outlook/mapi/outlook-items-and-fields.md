---
title: Campos e itens do Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 71c67c37cc4f9cd3ddd7a55c37c4ebd6ddd35cfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768198"
---
# <a name="outlook-items-and-fields"></a>Campos e itens do Outlook

  
  
**Aplica-se a**: Outlook 
  
Microsoft Outlook fornece os tipos de itens que são especializados para sua funcionalidade (por exemplo, itens de email, compromissos, contatos, tarefas e anotações). Outlook fornece campos padrão para cada tipo de item, normalmente conhecido como campos internos. Outlook também permite aos usuários criar campos personalizados, comumente conhecidos como campos definidos pelo usuário. Cada campo é associado um tipo de dados e um valor. Exemplos dos tipos de dados são **moeda**, **Data/hora**, **duração**, **Integer**, **palavras-chave**e **texto**. Os usuários podem definir campos personalizados usando o Designer de formulários do Outlook.
  
No nível de programação, cada item é representado por um objeto [IMessage](imessageimapiprop.md) . Cada campo definido pelo usuário é associado uma definição de campo e um valor. 
  
### <a name="field-definition"></a>Definição de campo

Uma definição de campo inclui o nome, tipo de dados e outras informações sobre o campo. Para cada item, o Outlook armazena as definições de todos os campos definidos pelo usuário na propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) do objeto **IMessage** correspondente. A propriedade **PidLidPropertyDefinitionStream** contém um fluxo binário conhecido como [PropertyDefinition](propertydefinition-stream-structure.md) que contém as definições de campo. Para obter mais informações sobre as estruturas de fluxo de definições de campo, consulte [Estruturas de Stream](stream-structures.md).
  
### <a name="field-value"></a>Valor do campo

Cada campo definido pelo usuário de um item tem um valor que é armazenado em uma propriedade denominada correspondente. Que a propriedade nomeada está no conjunto de propriedades PS_PUBLIC_STRINGS e tem uma cadeia de caracteres Unicode como o nome da propriedade. O tipo de dados da propriedade corresponde ao tipo de campo. Se a propriedade não estiver presente no objeto **IMessage** , o Outlook pressupõe um valor razoável padrão para a propriedade. Por exemplo, para um tipo de cadeia de caracteres, Outlook assume uma cadeia de caracteres vazia se a propriedade não estiver presente. 
  
## <a name="see-also"></a>Confira também



[Adicionar uma definição de um novo campo definido pelo usuário](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemplo de fluxo de PropertyDefinition](propertydefinition-stream-sample.md)
  
[Estruturas de fluxo](stream-structures.md)
  
[Estrutura de fluxo de PropertyDefinition](propertydefinition-stream-structure.md)
  
[Estrutura de fluxo de FieldDefinition](fielddefinition-stream-structure.md)
  
[Estrutura de fluxo de SkipBlock](skipblock-stream-structure.md)
  
[Estrutura de fluxo de FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
  
[Estrutura de fluxo de PackedAnsiString](packedansistring-stream-structure.md)
  
[Estrutura de fluxo de PackedUnicodeString](packedunicodestring-stream-structure.md)

