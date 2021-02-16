---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423661"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de conteúdo, que é usada para limitar um exibição de tabela apenas às linhas que incluem uma coluna com conteúdo correspondente a uma cadeia de caracteres de pesquisa. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a>Members

**ulFuzzyLevel**
  
> Configurações de opção que definem o nível de precisão que a restrição de conteúdo deve impor quando você verifica se há uma combinação.
    
   Os **16 bits** inferiores do **membro ulFuzzyLevel** se aplicam às propriedades do tipo PT_BINARY e PT_STRING8 e devem ser definidos com um dos seguintes valores: 
    
   - FL_FULLSTRING: para corresponder, a cadeia de caracteres de pesquisa **lpProp** deve estar contida na propriedade identificada por **ulPropTag**.
        
   - FL_PREFIX : para corresponder, a cadeia de caracteres de pesquisa **lpProp** deve aparecer no início da propriedade identificada por **ulPropTag**. As duas cadeias de caracteres devem ser comparadas apenas até o comprimento da cadeia de caracteres de pesquisa indicada por **lpProp**. 
        
   - FL_SUBSTRING: para corresponder, a cadeia de caracteres de pesquisa **lpProp** deve estar contida em qualquer lugar na propriedade identificada por **ulPropTag**. 
        
   Os **16 bits** superiores do membro **ulFuzzyLevel** se aplicam somente às propriedades do tipo PT_STRING8 e podem ser definidos com os seguintes valores em qualquer combinação: 
        
   - FL_IGNORECASE: a comparação deve ser feita sem considerar o caso. 
        
   - FL_IGNORENONSPACE: a comparação deve ignorar caracteres não espaçamento definidos por Unicode, como marcas diacríticas. 
        
   - FL_LOOSE: a comparação deve lhe dar uma combinação sempre que possível, ignorando caracteres sem espaçamento. 
    
**ulPropTag**
  
> Marca de propriedade que identifica a propriedade de cadeia de caracteres a ser verificada para a ocorrência da cadeia de caracteres de pesquisa. 
    
**lpProp**
  
> Ponteiro para uma estrutura de valores de propriedade que contém o valor de cadeia de caracteres a ser usado como a cadeia de caracteres de pesquisa.
    
## <a name="remarks"></a>Comentários

Há duas marcas de propriedade em uma estrutura **SContentRestriction:** uma no membro **ulPropTag** e outra no membro **ulPropTag** da estrutura **SPropValue** apontada por **lpProp**. Em ambas as marcas, MAPI requer apenas o campo de tipo de propriedade e ignora o campo do identificador de propriedade. No entanto, os dois tipos de propriedade devem corresponder ou o valor de erro MAPI_E_TOO_COMPLEX é retornado quando a restrição é usada em uma chamada para [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md). 
  
Os valores FL_FULLSTRING, FL_PREFIX e FL_SUBSTRING são mutuamente exclusivos. Apenas um deles pode ser definido, e um deles deve ser definido. Seus significados são corrigidos, e o provedor deve implementá-los exatamente como definido. O provedor deve retornar MAPI_E_TOO_COMPLEX se não puder dar suporte a esses valores. 
  
Os valores FL_IGNORECASE, FL_IGNORENONSPACE e FL_LOOSE são independentes. Qualquer lugar, de zero a todos os três, pode ser definido. Suas definições são fornecidas apenas como uma diretriz, e o provedor é livre para implementar seu próprio significado específico de cada sinalizador. O provedor não deve retornar nenhuma indicação de erro se não tiver nenhuma implementação de um sinalizador especificado. 
  
O resultado de uma restrição de conteúdo imposta a uma propriedade é indefinido quando a propriedade não existe. Quando um cliente exige um comportamento bem definido para essa restrição e não tem certeza se a propriedade existe, por exemplo, não é uma coluna necessária de uma tabela, ele deve criar uma restrição **AND** para ingressar na restrição de conteúdo com uma restrição existente. Use uma [estrutura SExistRestriction](sexistrestriction.md) para definir a restrição existente e uma [estrutura SAndRestriction](sandrestriction.md) para definir a **restrição AND.** 
  
For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Confira também

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [Estruturas MAPI](mapi-structures.md)

