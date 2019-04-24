---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtém a próxima conta no enumerador.
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321893"
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
  
> no Um ponteiro para uma interface **IUnknown** que o cliente pode consultar para obter uma interface [IOlkAccount](iolkaccount.md) . 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|S_FALSE  <br/> |O enumerador atingiu o fim.  <br/> |
   
## <a name="remarks"></a>Comentários

A interface especificada por *ppunk* herda de **IUnknown**. O cliente pode consultar esta interface (usando **IUnknown:: QueryInterface**) para obter um ponteiro para uma interface **IOlkAccount** e obter ou definir informações para essa conta. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

