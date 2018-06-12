---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Obtém o valor da propriedade conta especificada.
ms.openlocfilehash: 2c0756f416a209d37eff2209a82c298837f85f3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765908"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

Obtém o valor da propriedade conta especificada.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Par�metros

_dwProp_
  
> [in] A marca de propriedade da propriedade a conta a ser obtida.
    
_pVar_
  
> [out] O valor da propriedade especificada.
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |A propriedade não foi encontrada para a conta de determinado.  <br/> |
|E_INVALIDARG  <br/> |Uma marca de propriedade inválido foi especificada.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Depois que esse método retorna, se o valor da propriedade conta é um tipo binário ou cadeia de caracteres, você deve liberar *pVar* usando [IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

