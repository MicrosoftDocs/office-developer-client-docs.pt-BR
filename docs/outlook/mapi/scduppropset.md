---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8bbe8aa00ce446d228c23e1d474fa5140ae7b40a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581976"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Duplica uma matriz de valores de propriedade em um único bloco de memória MAPI combinar as operações das funções [ScCopyProps](sccopyprops.md) e [ScCountProps](sccountprops.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a>Parâmetros

 _cprop_
  
> [in] Contagem de valores de propriedade na matriz indicado pelo parâmetro _rgprop_ . 
    
 _rgprop_
  
> [in] Ponteiro para uma matriz de estruturas de [SPropValue](spropvalue.md) como definir os valores de propriedade a ser duplicado. 
    
 _lpAllocateBuffer_
  
> [in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória para a matriz duplicada. 
    
 _prgprop_
  
> [out] Ponteiro para a posição inicial na memória em que a matriz retornada de duplicada de estruturas de **SPropValue** está armazenada. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    

