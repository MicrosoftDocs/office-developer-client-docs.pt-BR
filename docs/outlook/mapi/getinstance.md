---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f65f047a73a2c06ca02251c554e5dca42352b6c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766665"
---
# <a name="getinstance"></a>GetInstance

  
  
**Aplica-se a**: Outlook 
  
Copia um valor dentro de uma propriedade de vários valores para uma propriedade de valor único do mesmo tipo. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIUTIL. H  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>Parâmetros

 _pvalMv_
  
> [in] Ponteiro para uma estrutura [SPropValue](spropvalue.md) definindo uma propriedade de valores múltiplos. 
    
 _pvalSv_
  
> [in] Ponteiro para uma propriedade de valor único para receber dados. 
    
 _uliInst_
  
> [in] O número de instância, ou seja, o elemento de matriz, do valor que está sendo copiado da estrutura de indicado pelo parâmetro _pvalMv_ . 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Se o valor copiado for muito grande para a memória alocada, a função **GetInstance** copia somente ponteiros em vez de alocar nova memória. 
  

