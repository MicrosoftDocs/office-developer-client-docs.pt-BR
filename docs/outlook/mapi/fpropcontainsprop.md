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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432627"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois valores de propriedade, geralmente cadeias de caracteres ou matrizes binárias, para ver se um contém o outro. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
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
  
> [in] Ponteiro para uma [estrutura SPropValue](spropvalue.md) definindo o valor da propriedade que pode conter a cadeia de caracteres de pesquisa apontado pelo _parâmetro lpSPropValueSrc._ 
    
_lpSPropValueSrc_
  
> [in] Ponteiro para uma **estrutura SPropValue** definindo a cadeia de caracteres de pesquisa que **FPropContainsProp** está procurando no valor de propriedade apontado pelo _parâmetro lpSPropValueDst._ 
    
_ulFuzzyLevel_
  
> [in] Configurações de opção que definem o nível de precisão a ser usado na comparação. 

  - Os **16 bits** inferiores se aplicam às propriedades do tipo PT_BINARY e PT_STRING8. Eles devem ser definidos com exatamente um dos seguintes valores:
      
    - FL_FULLSTRING: a cadeia de caracteres de pesquisa  _lpSPropValueSrc_ deve ser igual ao valor da propriedade identificado por  _lpSPropValueDst_.
        
    - FL_PREFIX: a cadeia de caracteres de pesquisa  _lpSPropValueSrc_ deve aparecer no início do valor da propriedade identificado por  _lpSPropValueDst_. Os dois valores devem ser comparados apenas até o comprimento da cadeia de caracteres de pesquisa indicado por  _lpSPropValueSrc_. 
        
    - FL_SUBSTRING: a cadeia de caracteres de pesquisa  _lpSPropValueSrc_ deve estar contida em qualquer lugar no valor da propriedade identificado por  _lpSPropValueDst_. 
      
  - Os **16 bits superiores** se aplicam somente às propriedades do tipo PT_STRING8. Eles podem ser definidos com os seguintes valores em qualquer combinação:
    
    - FL_IGNORECASE: a comparação deve ser feita sem considerar a sensibilidade a casos. 
        
    - FL_IGNORENONSPACE: a comparação deve ignorar caracteres não espaçamento definidos por Unicode, como marcas diacríticas. 
        
    - FL_LOOSE: a comparação deve indicar uma comparação sempre que possível, ignorando caracteres sem espaçamento e sensibilidade a letras.
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> Os parâmetros são todos válidos e a cadeia de caracteres de pesquisa _lpSPropValueSrc_ está contida conforme especificado no valor da propriedade _lpSPropValueDst._ 
    
FALSE 
  
> Os valores de propriedade que estão sendo comparados não são do tipo PT_STRING8 ou PT_BINARY, os valores de propriedade são de tipos diferentes ou a cadeia de caracteres de pesquisa _lpSPropValueSrc_ não está contida conforme especificado no valor da propriedade _lpSPropValueDst._ 
    
## <a name="remarks"></a>Comentários

O método de comparação depende dos tipos de propriedade especificados nas definições de propriedade [SPropValue](spropvalue.md) e da heurística de nível difusa fornecida no _parâmetro ulFuzzyLevel._ As [funções FPropCompareProp](fpropcompareprop.md) e **FPropContainsProp** podem ser usadas para preparar restrições para gerar uma tabela. 
  
Os 16 bits superiores de  _ulFuzzyLevel_ são ignorados para o tipo de PT_BINARY. Se as configurações em  _ulFuzzyLevel_ estão ausentes ou inválidas, uma sequência de caracteres completa exata é executada. Para obter mais informações sobre a propriedade de contenção, consulte a [estrutura SContentRestriction.](scontentrestriction.md) 
  

