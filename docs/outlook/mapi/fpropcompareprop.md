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
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427154"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois valores de propriedade usando um operador relacional especificado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>Parâmetros

_lpSPropValue1_
  
> [in] Ponteiro para uma [estrutura SPropValue](spropvalue.md) definindo o primeiro valor de propriedade para comparação. 
    
_ulRelOp_
  
> [in] O operador relacional a ser usado na comparação. Para valores permitidas, consulte a [estrutura SComparePropsRestriction.](scomparepropsrestriction.md) 
    
_lpSPropValue2_
  
> [in] Ponteiro para uma **estrutura SPropValue** definindo o segundo valor de propriedade para comparação. 
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> Os valores da propriedade satisfazem a relação especificada. 
    
FALSE 
  
> Os valores da propriedade não satisfazem a relação especificada.
    
## <a name="remarks"></a>Comentários

O método de comparação depende dos tipos de propriedade especificados nas definições de propriedade [SPropValue.](spropvalue.md) As **funções FPropCompareProp** e [FPropContainsProp](fpropcontainsprop.md) podem ser usadas para preparar restrições para gerar uma tabela. 
  
A ordem de comparação é  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _. Se os tipos de propriedade dos valores de propriedade a serem comparados não corresponderem, a **função FPropCompareProp** retornará FALSE. 
  

