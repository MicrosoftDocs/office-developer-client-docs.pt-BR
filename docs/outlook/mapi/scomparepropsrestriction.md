---
title: SComparePropsRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SComparePropsRestriction
api_type:
- COM
ms.assetid: 3231a91a-1ef2-4dd8-9f3e-79ca56d2eae9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7177b2f0f709939b7580fa7abb87490073bb00c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588808"
---
# <a name="scomparepropsrestriction"></a>SComparePropsRestriction

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de propriedade de comparação, qual testa duas propriedades usando um operador relacional. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a>Members

**RelOp**
  
> Operador relacional a ser usado para comparar as duas propriedades. Os valores possíveis são:
    
  - RELOP_GE: A comparação é feita com base no primeiro um valor maior ou igual.
      
  - RELOP_GT: A comparação é feita com base em um valor maior de primeiro.
      
  - RELOP_LE: A comparação é feita com base no primeiro um valor menor ou igual.
      
  - RELOP_LT: A comparação é feita com base em um valor menor de primeiro.
      
  - RELOP_NE: A comparação é feita com base nos valores desiguais.
      
  - RELOP_RE: A comparação é feita com base em como valores (expressão regular).
      
  - RELOP_EQ: A comparação é feita com base nos valores iguais.
    
**ulPropTag1**
  
> Marca de propriedade da primeira propriedade a ser comparada. 
    
**ulPropTag2**
  
> Marca de propriedade da segunda propriedade a ser comparada.
    
## <a name="remarks"></a>Comentários

A ordem de comparação é _(1) (operador relacional) de marca de propriedade (marca de propriedade 2)_. As propriedades a serem comparadas devem ser do mesmo tipo. Faz com que tentando comparar propriedades de diferentes tipos de MAPI ou o provedor de serviços para retornar o valor de erro MAPI_E_TOO_COMPLEX do método [IMAPITable](imapitableiunknown.md) ao qual a estrutura é passada como um parâmetro. 
  
O resultado de uma restrição de valor de propriedade de comparação é indefinido quando uma ou ambas as propriedades não existem. Quando um cliente exige comportamento bem definido para uma restrição tal e não é certeza se a propriedade existe (por exemplo, não é uma coluna obrigatória de uma tabela) deve criar uma restrição de **e** para ingressar a restrição de propriedade comparar com um existe restrição. Use uma estrutura de [SExistRestriction](sexistrestriction.md) para definir a restrição existe e uma estrutura de [SAndRestriction](sandrestriction.md) para definir a restrição **AND** . 
  
As propriedades especificadas nos membros **ulPropTag1** e **ulPropTag2** podem ser valores múltiplos se o provedor de serviços lhe fornecer apoio. 
  
Para obter mais informações sobre a estrutura de **SComparePropsRestriction** e restrições em geral, consulte [Sobre restrições](about-restrictions.md).
  
## <a name="see-also"></a>Confira também

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [Estruturas MAPI](mapi-structures.md)

