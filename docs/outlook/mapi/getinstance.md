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
ms.openlocfilehash: c4e5d2847b53988fb75e23fc6c4dfc386ea678f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579260"
---
# <a name="getinstance"></a>GetInstance

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  

