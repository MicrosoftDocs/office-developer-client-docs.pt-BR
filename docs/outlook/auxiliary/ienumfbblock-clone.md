---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Cria uma cópia do enumerador, usando a mesma restrição de tempo, mas definindo o cursor para o início do enumerador.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413399"
---
# <a name="ienumfbblockclone"></a>IEnumFBBlock::Clone

Cria uma cópia do enumerador, usando a mesma restrição de tempo, mas definindo o cursor para o início do enumerador.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a>Parâmetros

_ppcasa_
  
> [out] Um ponteiro para ponteiro para a cópia da interface [IEnumFBBlock.](ienumfbblock.md) 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_OUTOFMEMORY  <br/> |Há memória insuficiente para fazer a cópia.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Constantes (API do serviço de disponibilidade)](constants-free-busy-api.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

