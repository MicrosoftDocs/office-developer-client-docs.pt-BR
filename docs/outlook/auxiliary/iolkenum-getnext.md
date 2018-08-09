---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtém a próxima conta no enumerador.
ms.openlocfilehash: 496a4d787916d051c051b3a19a7113d9d50c6fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765999"
---
# <a name="iolkenumgetnext"></a>IOlkEnum::GetNext

Obtém a próxima conta no enumerador.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a>Parâmetros

_ppunk_
  
> [in] Um ponteiro para uma interface **IUnknown** que o cliente pode consultar para obter uma interface [IOlkAccount](iolkaccount.md) . 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|S_FALSE  <br/> |O enumerador atingiu o final.  <br/> |
   
## <a name="remarks"></a>Comentários

A interface especificada por *ppunk* herda de **IUnknown**. O cliente pode consultar a esta interface (usando **IUnknown:: QueryInterface**) para obter um ponteiro para uma interface **IOlkAccount** e obter ou definir informações para essa conta. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

