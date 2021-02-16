---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Obtém o valor da propriedade de conta especificada.
ms.openlocfilehash: d24df8cfa9d54bee4614c1f31e12268748b8c986
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433735"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

Obtém o valor da propriedade de conta especificada.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parâmetros

_dwProp_
  
> [in] A marca de propriedade da propriedade da conta a ser obter.
    
_pVar_
  
> [out] O valor da propriedade especificada.
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |A propriedade não foi encontrada para a conta determinada.  <br/> |
|E_INVALIDARG  <br/> |Uma marca de propriedade inválida foi especificada.  <br/> |
   
## <a name="remarks"></a>Comentários

Depois que esse método retornar, se o valor da propriedade da conta for um tipo binário ou de cadeia de caracteres, você deverá liberar  *pVar*  usando [IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

