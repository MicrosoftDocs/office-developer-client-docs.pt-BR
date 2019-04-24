---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Obtém o próximo número específico de blocos de disponibilidade de dados em uma enumeração.
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319590"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

Obtém o próximo número específico de blocos de disponibilidade de dados em uma enumeração.
  
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
  
> no O número de blocos de dados de disponibilidade no *pblk* a serem recuperados. 
    
_pblk_
  
> no Um ponteiro para uma matriz de blocos de disponibilidade. A matriz é alocada com um tamanho de *celt* . Os blocos de disponibilidade solicitados são retornados nessa matriz. 
    
_pcfetch_
  
> bota O número de blocos de disponibilidade realmente retornados no *pblk* . 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |O número solicitado de blocos foi retornado.  <br/> |
|S_FALSE  <br/> |O número solicitado de blocos não foi retornado.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Constantes (API do serviço de disponibilidade)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

