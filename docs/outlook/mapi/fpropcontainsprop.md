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
ms.openlocfilehash: b08d3af8c61d8ced31e822bb787d49ad90b4df54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571672"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois valores de propriedade, geralmente as cadeias de caracteres ou matrizes de binários, para ver se um contém o outro. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>Parâmetros

_lpSPropValueDst_
  
> [in] Ponteiro para uma estrutura [SPropValue](spropvalue.md) definindo o valor da propriedade que pode conter a cadeia de caracteres de pesquisa apontado pelo parâmetro _lpSPropValueSrc_ . 
    
_lpSPropValueSrc_
  
> [in] Ponteiro para uma estrutura **SPropValue** definindo a cadeia de caracteres de pesquisa que **FPropContainsProp** está procurando no valor da propriedade apontado pelo parâmetro _lpSPropValueDst_ . 
    
_ulFuzzyLevel_
  
> [in] Configurações de opção definindo o nível de precisão para usar na comparação. 

  - Os **16 bits inferiores** se aplicam às propriedades do tipo PT_BINARY e PT_STRING8. Eles devem ser definidos como exatamente um dos seguintes valores:
      
    - FL_FULLSTRING: A cadeia de caracteres de pesquisa _lpSPropValueSrc_ deve ser igual ao valor da propriedade identificado pela _lpSPropValueDst_.
        
    - FL_PREFIX: A cadeia de caracteres de pesquisa _lpSPropValueSrc_ deverá aparecer no início do valor da propriedade identificado pela _lpSPropValueDst_. Os dois valores devem ser comparados somente até o comprimento da cadeia de caracteres de pesquisa indicado pelo _lpSPropValueSrc_. 
        
    - FL_SUBSTRING: A cadeia de caracteres de pesquisa _lpSPropValueSrc_ deve estar contida em qualquer lugar no valor da propriedade identificado pela _lpSPropValueDst_. 
      
  - Os **bits de 16 superiores** aplicam-se apenas às propriedades do tipo PT_STRING8. Elas podem ser definidas para os seguintes valores em qualquer combinação:
    
    - FL_IGNORECASE: Comparação deve ser feita sem considerar a diferenciação de maiusculas. 
        
    - FL_IGNORENONSPACE: Comparação deve ignorar caracteres sem espaçamento definidos pelo Unicode, como sinais diacríticos. 
        
    - FL_LOOSE: Comparação deve indicar uma correspondência sempre que possível, ignorando caso sensibilidade e caracteres sem espaçamento.
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> Os parâmetros são válidos e a cadeia de caracteres de pesquisa _lpSPropValueSrc_ está contida conforme especificado no valor da propriedade _lpSPropValueDst_ . 
    
FALSO 
  
> Os valores de propriedade estão sendo comparados não são do tipo PT_STRING8 ou PT_BINARY, os valores de propriedade são de tipos diferentes ou a cadeia de caracteres de pesquisa _lpSPropValueSrc_ não está contida conforme especificado no valor da propriedade _lpSPropValueDst_ . 
    
## <a name="remarks"></a>Comentários

O método de comparação depende os tipos de propriedade especificados nas definições de propriedade [SPropValue](spropvalue.md) e o heurístico nível difuso fornecido no parâmetro _ulFuzzyLevel_ . As funções [FPropCompareProp](fpropcompareprop.md) e **FPropContainsProp** podem ser usadas para preparar restrições para gerar uma tabela. 
  
Os 16 bits superiores _ulFuzzyLevel_ são ignorados para o tipo de propriedade PT_BINARY. Se as configurações no _ulFuzzyLevel_ ausente ou inválido, uma correspondência exata da cadeia de caracteres inteira é executada. Para obter mais informações sobre contenção de propriedade, consulte a estrutura [SContentRestriction](scontentrestriction.md) . 
  

