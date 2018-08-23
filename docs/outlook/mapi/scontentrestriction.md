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
ms.openlocfilehash: 43703051193ffacec6a54355eeea74edf904f186
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580569"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de conteúdo, que é usada para limitar a um modo de exibição tabela apenas as linhas que incluem uma coluna com a correspondência de uma cadeia de caracteres de pesquisa de conteúdo. 
  
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
  
> Configurações de opção definindo o nível de precisão a restrição de conteúdo imponha quando você verificar por uma correspondência.
    
   Os **16 bits inferiores** do membro **ulFuzzyLevel** se aplicam às propriedades do tipo PT_BINARY e PT_STRING8 e deve ser definida como um dos seguintes valores: 
    
   - FL_FULLSTRING: Para corresponder, a cadeia de caracteres de pesquisa **lpProp** deve estar contida na propriedade identificada pela **ulPropTag**.
        
   - FL_PREFIX: Para corresponder, a cadeia de caracteres de pesquisa **lpProp** deverá aparecer no início da propriedade identificado pela **ulPropTag**. As duas cadeias de caracteres devem ser comparadas somente até o comprimento da cadeia de caracteres de pesquisa indicado pelo **lpProp**. 
        
   - FL_SUBSTRING: Para corresponder, a cadeia de caracteres de pesquisa **lpProp** deve estar contida em qualquer lugar na propriedade identificada pela **ulPropTag**. 
        
   Os **16 bits superiores** do membro **ulFuzzyLevel** aplicam-se apenas às propriedades do tipo PT_STRING8 e pode ser definida para os seguintes valores em qualquer combinação: 
        
   - FL_IGNORECASE: Comparação deve ser feita sem considerar caso. 
        
   - FL_IGNORENONSPACE: Comparação deve ignorar caracteres de sem espaçamento definido pelo Unicode como sinais diacríticos. 
        
   - FL_LOOSE: Comparação deve fornecer uma correspondência sempre que possível, ignorando caso e caracteres sem espaçamento. 
    
**ulPropTag**
  
> Marca de propriedade que identifica a propriedade de cadeia de caracteres a ser verificado para ocorrência da cadeia de caracteres de pesquisa. 
    
**lpProp**
  
> Ponteiro para uma estrutura de valor de propriedade que contém o valor de cadeia de caracteres a ser usado como a cadeia de caracteres de pesquisa.
    
## <a name="remarks"></a>Comentários

Há duas marcas de propriedade em uma estrutura de **SContentRestriction** : um membro do **ulPropTag** e o outro no membro **ulPropTag** da estrutura **SPropValue** apontado pela **lpProp**. Em ambas as marcas, MAPI exige apenas o campo de tipo de propriedade e ignora o campo do identificador de propriedade. No entanto, os tipos de dois propriedade devem corresponder, caso contrário, o valor de erro MAPI_E_TOO_COMPLEX é retornado quando a restrição é usada em uma chamada para [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md). 
  
Os valores FL_FULLSTRING, FL_PREFIX e FL_SUBSTRING são mutuamente exclusivos. Apenas um deles pode ser definido e um deles deve ser definido. Seus significados corrigidos e o provedor deve implementá-los exatamente conforme definido. O provedor deve retornar MAPI_E_TOO_COMPLEX se não for possível dar suporte a esses valores. 
  
Os valores FL_IGNORECASE, FL_IGNORENONSPACE e FL_LOOSE são independentes. Em qualquer lugar do zero para todos os três deles pode ser definido. Suas definições são fornecidas como uma diretriz apenas e o provedor é livre para implementar seu próprio significado específico de cada sinalizador. O provedor não deve retornar qualquer indicação de erro, se ele tiver nenhuma implementação de um sinalizador especificado. 
  
O resultado de uma restrição imposta em relação a uma propriedade de conteúdo é indefinido quando a propriedade não existe. Quando um cliente exige comportamento bem definido para uma restrição tal e não é certeza se a propriedade existe por exemplo, não é uma coluna obrigatória de uma tabela, ele deve criar uma restrição de **e** para ingressar a restrição de conteúdo com uma restrição existe. Use uma estrutura de [SExistRestriction](sexistrestriction.md) para definir a restrição existe e uma estrutura de [SAndRestriction](sandrestriction.md) para definir a restrição **AND** . 
  
Para obter mais informações sobre a estrutura de **SContentRestriction** e restrições em geral, consulte [Sobre restrições](about-restrictions.md).
  
## <a name="see-also"></a>Confira também

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [Estruturas MAPI](mapi-structures.md)

