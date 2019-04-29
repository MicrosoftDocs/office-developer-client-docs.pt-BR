---
title: Estrutura de fluxo PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438586"
---
# <a name="propertydefinition-stream-structure"></a>Estrutura de fluxo PropertyDefinition

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma estrutura de fluxo do PropertyDefinition é uma matriz de estruturas de fluxo do [FieldDefinition](fielddefinition-stream-structure.md) que contêm definições para todos os campos definidos pelo usuário em um item do Microsoft Outlook e configurações de vinculação de dados para alguns campos internos. 
  
Você pode manipular programaticamente a estrutura de fluxo do PropertyDefinition. No enTanto, você pode obter resultados semelhantes usando o designer de formulários do Outlook e, em particular, a caixa de diálogo **Propriedades** para um controle associado a dados. 
  
As definições de campo em uma estrutura de fluxo do PropertyDefinition podem ser um dos dois formatos: PropDefV1 e PropDefV2. O Outlook oferece suporte ao PropDefV1 e ao PropDefV2. Todas as definições de campo em uma única estrutura de fluxo de PropertyDefinition devem ter o mesmo formato. Para obter mais informações sobre como PropDefV1 e PropDefV2 diferem, consulte [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).
  
Os elementos de dados neste fluxo são armazenados em uma ordem de byte little-endian, imediatamente após o outro na ordem especificada abaixo.
  
- Versão: WORD (2 bytes), o formato das definições de campo na estrutura de fluxo do PropertyDefinition. A tabela a seguir mostra os valores possíveis.
    
    |**Valor**|**Descrição**|
    |:-----|:-----|
    |0x0102  <br/> |O formato é PropDefV1.  <br/> |
    |0x0103  <br/> |O formato é PropDefV2.  <br/> |
   
- FieldDefinitionCount: DWORD (4 bytes), o número de definições de campo neste fluxo. Esta é a contagem dos elementos de matriz no elemento de dados FieldDefinitions.
    
- FieldDefinitions: uma matriz de estruturas de fluxo do FieldDefinition. A contagem dessa matriz é igual ao elemento de dados FieldDefinitionCount.
    
## <a name="see-also"></a>Confira também

- [Campos e itens do Outlook](outlook-items-and-fields.md)
- [Adicionar uma definição para um novo campo definido pelo usuário](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [Exemplo de fluxo PropertyDefinition](propertydefinition-stream-sample.md)
- [Estruturas de fluxo](stream-structures.md)

