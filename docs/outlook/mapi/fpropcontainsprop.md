---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328039"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois valores de propriedade, geralmente cadeias de caracteres ou matrizes binárias, para ver se um contém o outro. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>Parâmetros

_lpSPropValueDst_
  
> no Ponteiro para uma estrutura [SPropValue](spropvalue.md) que define o valor da propriedade que pode conter a cadeia de caracteres de pesquisa apontada pelo parâmetro _lpSPropValueSrc_ . 
    
_lpSPropValueSrc_
  
> no Ponteiro para uma estrutura **SPropValue** que define a cadeia de caracteres de pesquisa que **FPropContainsProp** está procurando no valor da propriedade apontado pelo parâmetro _lpSPropValueDst_ . 
    
_ulFuzzyLevel_
  
> no Configurações de opção que definem o nível de precisão a ser usado na comparação. 

  - Os **16 bits inferiores** se aplicam às propriedades do tipo PT_BINARY e PT_STRING8. Eles devem ser configurados exatamente como um dos seguintes valores:
      
    - FL_FULLSTRING: a cadeia de caracteres de pesquisa _lpSPropValueSrc_ deve ser igual ao valor da propriedade identificado por _lpSPropValueDst_.
        
    - FL_PREFIX: a cadeia de caracteres de pesquisa _lpSPropValueSrc_ deve aparecer no início do valor da propriedade identificado por _lpSPropValueDst_. Os dois valores devem ser comparados apenas até o comprimento da cadeia de caracteres de pesquisa indicada por _lpSPropValueSrc_. 
        
    - FL_SUBSTRING: a cadeia de caracteres de pesquisa _lpSPropValueSrc_ deve estar contida em qualquer lugar no valor da propriedade identificado por _lpSPropValueDst_. 
      
  - Os **16 bits superiores** se aplicam apenas às propriedades do tipo PT_STRING8. Eles podem ser definidos com os seguintes valores em qualquer combinação:
    
    - FL_IGNORECASE: a comparação deve ser feita sem considerar a confidencialidade de maiúsculas e minúsculas. 
        
    - FL_IGNORENONSPACE: a comparação deve ignorar caracteres não espaçados Unicode definidos como marcas diacríticos. 
        
    - FL_LOOSE: a comparação deve indicar uma coincidência sempre que possível, ignorando os caracteres de diferenciação de maiúsculas e minúsculas.
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> Os parâmetros são todos válidos e a cadeia de caracteres de pesquisa do _lpSPropValueSrc_ está contida como especificado no valor da propriedade _lpSPropValueDst_ . 
    
FALSE 
  
> Os valores de propriedade comparados não são do tipo PT_STRING8 ou PT_BINARY, os valores de propriedade são de tipos diferentes ou a sequência de caracteres de pesquisa do _lpSPropValueSrc_ não está contida como especificado no valor da propriedade _lpSPropValueDst_ . 
    
## <a name="remarks"></a>Comentários

O método Comparison depende dos tipos de propriedade especificados nas definições de propriedade [SPropValue](spropvalue.md) e o heurístico de nível difuso fornecido no parâmetro _ulFuzzyLevel_ . As funções [FPropCompareProp](fpropcompareprop.md) e **FPropContainsProp** podem ser usadas para preparar restrições para a geração de uma tabela. 
  
Os 16 bits superiores de _ulFuzzyLevel_ são ignorados para o tipo de propriedade PT_BINARY. Se as configurações no _ulFuzzyLevel_ estiverem ausentes ou forem inválidas, uma correspondência exata de cadeia de caracteres completa será executada. Para obter mais informações sobre a contenção de propriedade, consulte a estrutura [SContentRestriction](scontentrestriction.md) . 
  

