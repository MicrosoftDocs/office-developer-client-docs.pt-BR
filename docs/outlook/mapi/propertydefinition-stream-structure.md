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
  
Uma estrutura de fluxo PropertyDefinition é uma matriz de estruturas de fluxo [FieldDefinition](fielddefinition-stream-structure.md) que contêm definições para todos os campos definidos pelo usuário em um item do Microsoft Outlook e configurações de vinculação de dados para alguns campos integrados. 
  
Você pode manipular programaticamente a estrutura de fluxo PropertyDefinition. No entanto, você pode obter resultados semelhantes usando o  Designer de Formulários do Outlook e, em particular, a caixa de diálogo Propriedades para um controle vinculado a dados. 
  
As definições de campo em uma estrutura de fluxo PropertyDefinition podem ser um dos dois formatos: PropDefV1 e PropDefV2. O Outlook dá suporte a PropDefV1 e PropDefV2. Todas as definições de campo em uma única estrutura de fluxo PropertyDefinition devem ter o mesmo formato. Para obter mais informações sobre como PropDefV1 e PropDefV2 diferem, consulte [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).
  
Os elementos de dados nesse fluxo são armazenados em ordem de byte little-endian, imediatamente após uns aos outros na ordem especificada abaixo.
  
- Versão: WORD (2 bytes), o formato das definições de campo na estrutura de fluxo PropertyDefinition. A tabela a seguir mostra os valores possíveis.
    
    |**Valor**|**Descrição**|
    |:-----|:-----|
    |0x0102  <br/> |O formato é PropDefV1.  <br/> |
    |0x0103  <br/> |O formato é PropDefV2.  <br/> |
   
- FieldDefinitionCount: DWORD (4 bytes), o número de definições de campo neste fluxo. Esta é a contagem de elementos de matriz no elemento de dados FieldDefinitions.
    
- FieldDefinitions: uma matriz de estruturas de fluxo FieldDefinition. A contagem dessa matriz é igual ao elemento de dados FieldDefinitionCount.
    
## <a name="see-also"></a>Confira também

- [Campos e itens do Outlook](outlook-items-and-fields.md)
- [Adicionar uma definição para um novo User-Defined campo](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [Exemplo de fluxo propertyDefinition](propertydefinition-stream-sample.md)
- [Estruturas de fluxo](stream-structures.md)

