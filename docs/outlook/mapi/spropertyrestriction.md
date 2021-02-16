---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 29d392eba530126e06a672c10044c5b4df0618c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406084"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de propriedade que é usada para corresponder a uma constante com o valor de uma propriedade.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a>Members

**re ltda**
  
> Operador relacional que será usado na pesquisa. Os valores possíveis são:
    
  - RELOP_GE: a comparação é feita com base em um primeiro valor maior ou igual.
        
  - RELOP_GT: a comparação é feita com base em um primeiro valor maior.
        
  - RELOP_LE: a comparação é feita com base em um primeiro valor menor ou igual.
        
  - RELOP_LT: a comparação é feita com base em um primeiro valor menor.
        
  - RELOP_NE: a comparação é feita com base em valores de valores de valores diferentes.
        
  - RELOP_RE: a comparação é feita com base nos valores LIKE (expressão regular).
        
  - RELOP_EQ: a comparação é feita com base em valores iguais.
    
**ulPropTag**
  
> Marca de propriedade que identifica a propriedade a ser comparada. 
    
**lpProp**
  
> Ponteiro para uma [estrutura SPropValue](spropvalue.md) que contém o valor constante que será usado na comparação. 
    
## <a name="remarks"></a>Comentários

Há duas marcas de propriedade em uma **estrutura SPropertyRestriction.** Um está no **membro ulPropTag** e o outro está no membro **ulPropTag** da estrutura **SPropValue** apontado por **lpProp**. MAPI requires both the property identifier field and the property type field. **UlPropTag** em **SPropertyRestriction** é a propriedade a ser matched, e o ponteiro **lpProp** do **SPropertyRestriction** para o tipo de **ulPropTag** do **SPropValue** indica como o valor de membros da união **lpProp** são interpretados. Os dois tipos de propriedade devem corresponder ou o valor de erro MAPI_E_TOO_COMPLEX é retornado quando a restrição é usada em uma chamada para [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md). 
  
A ordem de comparação _é (valor da propriedade) (operador relacional) (valor constante)._
  
Quando uma restrição de propriedade é passada para **IMAPITable::Restrict** ou **IMAPITable::FindRow** e a propriedade de destino não existe, os resultados da restrição são indefinido. Ao criar uma **restrição AND** que une a restrição de propriedade com uma restrição **EXIST,** um chamador pode ter resultados precisos garantidos. Use uma [estrutura SExistRestriction](sexistrestriction.md) para definir a restrição **EXIST** e uma [estrutura SAndRestriction](sandrestriction.md) para definir a **restrição AND.** 
  
As marcas de propriedade de valores múltiplos poderão ser usadas nas restrições de propriedade se o provedor de serviços que implementa a tabela as suportar. Se tiver suporte, as marcas de propriedade de vários valores podem ser usadas em qualquer lugar que as marcas de propriedade de valor único possam ser usadas. 
  
Marcas de propriedade de valores múltiplos podem ser usadas nos seguintes métodos:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Um caso notável quando as duas marcas de propriedade não corresponderem é se estiver restringindo uma propriedade de vários valores. Nesse caso, o seguinte deve ser verdadeiro. > Se o tipo de propriedade **da ulPropTag** de **SPropertyRestriction** contiver o sinalizador de bit do tipo de propriedade de vários valores MV_FLAG (0x1000), o tipo de propriedade **do ulPropTag** de **SPropValue** deverá corresponder ao primeiro menos o sinalizador de bit MV_FLAG, ou seja, seu inverso. > Por exemplo, para restringir o uso de uma propriedade de cadeia de caracteres personalizada de vários valores, como uma categoria com uma marca de propriedade para a propriedade 0x8012101f, ou seja, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), a **SPropertyRestriction** correspondente aparecerá da seguinte forma. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> observe que, se o tipo de propriedade **do ulPropTag** de **SPropValue** contiver o sinalizador MV_FLAG bit, o provável retorno será MAPI_E_TOO_COMPLEX. 
  
Para obter mais informações sobre a **estrutura SPropertyRestriction,** consulte [Sobre restrições](about-restrictions.md). 
  
## <a name="see-also"></a>Confira também

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::ExpandRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [Estruturas MAPI](mapi-structures.md)

