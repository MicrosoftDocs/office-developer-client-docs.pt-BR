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
ms.openlocfilehash: 513ec0db4e99e687d8aeb9e1d6acdef73df4d158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440000"
---
# <a name="scomparepropsrestriction"></a>SComparePropsRestriction

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de propriedade comparar, que testa duas propriedades usando um operador relacional. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Operador relacional a ser usado para comparar as duas propriedades. Os valores possíveis são os seguintes:
    
  - RELOP_GE: a comparação é feita com base em um valor maior ou igual a um primeiro.
      
  - RELOP_GT: a comparação é feita com base em um primeiro valor maior.
      
  - RELOP_LE: a comparação é feita com base em um valor menor ou igual a.
      
  - RELOP_LT: a comparação é feita com base em um primeiro valor menor.
      
  - RELOP_NE: a comparação é feita com base em valores desiguais.
      
  - RELOP_RE: a comparação é feita com base nos valores LIKE (expressão regular).
      
  - RELOP_EQ: a comparação é feita com base em valores iguais.
    
**ulPropTag1**
  
> Marca de propriedade da primeira propriedade a ser comparada. 
    
**ulPropTag2**
  
> Marca de propriedade da segunda Propriedade a ser comparada.
    
## <a name="remarks"></a>Comentários

A ordem de comparação é _(marca de propriedade 1) (operador relacional) (marca de propriedade 2)_. As propriedades a serem comparadas devem ser do mesmo tipo. Tentar comparar propriedades de tipos diferentes faz com que o MAPI ou o provedor de serviços retorne o valor de erro [](imapitableiunknown.md) MAPI_E_TOO_COMPLEX do método IMAPITable para o qual a estrutura é passada como um parâmetro. 
  
O resultado de uma restrição de valor de propriedade Compare é indefinido quando uma ou ambas as propriedades não existem. Quando um cliente requer um comportamento bem definido para tal restrição e não tem certeza se a propriedade existe, (por exemplo, não é uma coluna obrigatória de uma tabela), deve criar uma restrição para **** ingressar na restrição de propriedade Compare com uma existente restrição. Use uma estrutura [SExistRestriction](sexistrestriction.md) para definir a restrição existir e uma estrutura [SAndRestriction](sandrestriction.md) para definir a restrição **e** . 
  
As propriedades especificadas nos membros **ulPropTag1** e **ulPropTag2** podem ter vários valores se o provedor de serviços oferecer suporte a ela. 
  
Para obter mais informações sobre a estrutura e as restrições do **SComparePropsRestriction** em geral, consulte [about Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Confira também

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [Estruturas MAPI](mapi-structures.md)

