---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Define o valor da propriedade conta especificada.
ms.openlocfilehash: 2bb8a323f5f3399b9eac1cfdf9ac18faddfdb259
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765925"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

Define o valor da propriedade conta especificada.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parâmetros

_dwProp_
  
> [in] A marca de propriedade da propriedade conta para definir.
    
_pVar_
  
> [in] O valor da propriedade especificada.
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada do método foi bem-sucedida.  <br/> |
|E_INVALIDARG  <br/> |Uma marca de propriedade inválido foi especificada.  <br/> |
   
## <a name="remarks"></a>Comentários

Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) para salvar as alterações para o valor das propriedades de conta. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

