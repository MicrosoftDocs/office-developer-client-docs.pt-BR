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
ms.openlocfilehash: f59b0041f271010e56dda2f73d2248f133bc1325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770470"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**Aplica-se a**: Outlook 
  
Descreve uma restrição de propriedade que será usada para corresponder a uma constante com o valor de uma propriedade.
  
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

**RelOp**
  
> Operador relacional que será usado na pesquisa. Os valores possíveis são:
    
  - RELOP_GE: A comparação é feita com base no primeiro um valor maior ou igual.
        
  - RELOP_GT: A comparação é feita com base em um valor maior de primeiro.
        
  - RELOP_LE: A comparação é feita com base no primeiro um valor menor ou igual.
        
  - RELOP_LT: A comparação é feita com base em um valor menor de primeiro.
        
  - RELOP_NE: A comparação é feita com base nos valores desiguais.
        
  - RELOP_RE: A comparação é feita com base em como valores (expressão regular).
        
  - RELOP_EQ: A comparação é feita com base nos valores iguais.
    
**ulPropTag**
  
> Marca de propriedade que identifica a propriedade a ser comparada. 
    
**lpProp**
  
> Ponteiro para uma estrutura [SPropValue](spropvalue.md) que contém o valor da constante que será usado na comparação. 
    
## <a name="remarks"></a>Comentários

Há duas marcas de propriedade em uma estrutura **SPropertyRestriction** . Uma é no membro **ulPropTag** e o outro for no membro **ulPropTag** da estrutura **SPropValue** apontado pela **lpProp**. MAPI requer o campo do identificador de propriedade e um campo de tipo de propriedade. O **ulPropTag** em **SPropertyRestriction** é a propriedade a ser correspondido e o ponteiro de **lpProp** de **SPropertyRestriction** o tipo do **ulPropTag**do **SPropValue** indica como o valor de membros do União **lpProp** são interpretadas. Os tipos de dois propriedade devem corresponder, senão o valor de erro MAPI_E_TOO_COMPLEX é retornado quando a restrição é usada em uma chamada para [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md). 
  
A ordem de comparação é _(valor da propriedade) (operador relacional) (valor de constante)_.
  
Quando uma restrição de propriedade é passada para **IMAPITable:: Restrict** ou **IMAPITable:: FindRow** e a propriedade de destino não existir, os resultados da restrição são indefinidos. Criando uma restrição **AND** que une a restrição de propriedade com uma restrição **EXISTEM** , um chamador pode ser garantido resultados exatos. Use uma estrutura de [SExistRestriction](sexistrestriction.md) para definir a restrição **existe** e uma estrutura de [SAndRestriction](sandrestriction.md) para definir a restrição **AND** . 
  
Marcas de valores múltiplos de propriedade podem ser usadas em restrições de propriedade, se o provedor de serviço implementando a tabela oferece suporte a eles. Se houver suporte, marcas de propriedade de valores múltiplos podem ser marcas de propriedade de valor único podem ser usadas em qualquer lugar usadas. 
  
Marcas de propriedade de valores múltiplos podem ser usadas nos seguintes métodos:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Uma ocorrência notável quando as marcas de duas propriedade não coincidem com é se restringindo em uma propriedade de valor múltiplos. Nesse caso, a seguir deve ser verdadeira. > Se o tipo de propriedade do **ulPropTag** de **SPropertyRestriction** contém o sinalizador de bit de tipo de propriedade de valores múltiplos MV_FLAG (0x1000), o tipo de propriedade do **ulPropTag** de **SPropValue** deve corresponder ao primeiro menos o MV_ Sinalizador de bit de sinalizador, ou seja, seu inverso. > Por exemplo, para restringir usando uma propriedade de cadeia de caracteres de valores múltiplos personalizada, como uma categoria com uma marca de propriedade para a propriedade 0x8012101f, ou seja, PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012)), o correspondente **SPropertyRestriction** apareceria como segue. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Observe que, se o tipo de propriedade do **ulPropTag** de **SPropValue** contiver o sinalizador de bit MV_FLAG, o retorno provavelmente é MAPI_E_TOO_COMPLEX. 
  
Para obter mais informações sobre a estrutura **SPropertyRestriction** , consulte [Sobre restrições](about-restrictions.md). 
  
## <a name="see-also"></a>Confira também

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::ExpandRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [Estruturas MAPI](mapi-structures.md)

