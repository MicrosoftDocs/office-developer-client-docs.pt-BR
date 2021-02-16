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
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406014"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Duplica uma matriz de valores de propriedade em um único bloco de memória MAPI combinando as operações das funções [ScCopyProps](sccopyprops.md) e [ScCountProps.](sccountprops.md) 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
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
  
> [in] Contagem de valores de propriedade na matriz indicada pelo _parâmetro rgprop._ 
    
 _rgprop_
  
> [in] Ponteiro para uma matriz de [estruturas SPropValue](spropvalue.md) definindo os valores de propriedade a serem duplicados. 
    
 _lpAllocateBuffer_
  
> [in] Ponteiro para a [função MAPIAllocateBuffer,](mapiallocatebuffer.md) a ser usado para alocar memória para a matriz duplicada. 
    
 _prgprop_
  
> [out] Ponteiro para a posição inicial na memória onde a matriz duplicada retornada de **estruturas SPropValue** é armazenada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    

