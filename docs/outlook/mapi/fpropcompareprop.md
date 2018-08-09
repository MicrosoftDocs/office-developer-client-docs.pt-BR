---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 69bbed644a8173bf9291ca48a63960f693108318
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766608"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**Aplica-se a**: Outlook 
  
Compara dois valores de propriedade usando um operador relacional especificado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>Parâmetros

_lpSPropValue1_
  
> [in] Ponteiro para uma estrutura [SPropValue](spropvalue.md) definindo o valor da propriedade primeiro para comparação. 
    
_ulRelOp_
  
> [in] O operador relacional a ser usado na comparação. Para valores permitidos, consulte a estrutura [SComparePropsRestriction](scomparepropsrestriction.md) . 
    
_lpSPropValue2_
  
> [in] Ponteiro para uma estrutura **SPropValue** definindo o valor da propriedade segundo para comparação. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> Os valores de propriedade satisfazer o objeto relation especificado. 
    
FALSO 
  
> Os valores de propriedade não atenderem a relação especificada.
    
## <a name="remarks"></a>Comentários

O método de comparação depende os tipos de propriedade especificados nas definições de propriedade [SPropValue](spropvalue.md) . As funções **FPropCompareProp** e [FPropContainsProp](fpropcontainsprop.md) podem ser usadas para preparar restrições para gerar uma tabela. 
  
A ordem de comparação é _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _. Se os tipos de propriedade dos valores de propriedade a ser comparada não coincidirem, a função **FPropCompareProp** retorna FALSE. 
  

