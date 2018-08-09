---
title: Estrutura de fluxo de PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 289227ee171c2325cad0ed321dab4f635a0ca724
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770205"
---
# <a name="propertydefinition-stream-structure"></a>Estrutura de fluxo de PropertyDefinition

**Aplica-se a**: Outlook 
  
Uma estrutura de fluxo de PropertyDefinition é uma matriz de estruturas de fluxo de [FieldDefinition](fielddefinition-stream-structure.md) que contêm definições para todos os campos definidos pelo usuário em um item do Microsoft Outlook e configurações de associação de dados para alguns campos internos. 
  
Programaticamente, você pode manipular a estrutura de fluxo de PropertyDefinition. No entanto, você pode obter resultados semelhantes usando o Designer de formulários do Outlook e, em particular, a caixa de diálogo **Propriedades de** caixa de um controle acoplado a dados. 
  
Definições de campo em uma estrutura de fluxo de PropertyDefinition podem ser um dos dois formatos: PropDefV1 e PropDefV2. O Outlook suporta PropDefV1 e o PropDefV2. Todas as definições de campo em uma estrutura de fluxo de PropertyDefinition única devem ser do mesmo formato. Para obter mais informações sobre a diferença entre PropDefV1 e PropDefV2, consulte [FieldDefinition Stream estrutura](fielddefinition-stream-structure.md).
  
Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após a outra na ordem especificada abaixo.
  
- Versão: WORD (2 bytes), o formato das definições de campo no PropertyDefinition stream estrutura. A tabela a seguir mostra os valores possíveis.
    
    |**Valor**|**Descrição**|
    |:-----|:-----|
    |0x0102  <br/> |Formato é PropDefV1.  <br/> |
    |0x0103  <br/> |Formato é PropDefV2.  <br/> |
   
- FieldDefinitionCount: DWORD (4 bytes), o número de definições de campo neste fluxo. É a contagem de elementos de matriz em que o elemento de dados FieldDefinitions.
    
- FieldDefinitions: Uma matriz de estruturas de fluxo de FieldDefinition. A contagem dessa matriz é igual ao elemento FieldDefinitionCount dados.
    
## <a name="see-also"></a>Confira também

- [Campos e itens do Outlook](outlook-items-and-fields.md)
- [Adicionar uma definição de um novo campo definido pelo usuário](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [Exemplo de fluxo de PropertyDefinition](propertydefinition-stream-sample.md)
- [Estruturas de fluxo](stream-structures.md)

