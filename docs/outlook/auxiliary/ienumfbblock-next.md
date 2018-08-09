---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Obtém o próximo número especificado de blocos de informações de disponibilidade de dados em uma enumeração.
ms.openlocfilehash: ec366cf102d3c75487f9485cfae7764d68695f10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765826"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

Obtém o próximo número especificado de blocos de informações de disponibilidade de dados em uma enumeração.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a>Parâmetros

_celt_
  
> [in] O número de livre/ocupado dados blocos no *pblk* para recuperar. 
    
_PBLK_
  
> [in] Um ponteiro para uma matriz de blocos de livre/ocupado. A matriz é alocada um tamanho de *celt* . Os blocos de livre/ocupado solicitados são retornados nessa matriz. 
    
_pcfetch_
  
> [out] O número de blocos de livre/ocupado realmente retornados em *pblk* . 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |O número de blocos solicitado foi retornado.  <br/> |
|S_FALSE  <br/> |O número de blocos solicitado não foi retornado.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Constantes (API de livre/ocupado)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

