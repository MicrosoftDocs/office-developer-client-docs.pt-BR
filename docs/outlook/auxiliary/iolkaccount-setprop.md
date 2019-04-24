---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Define o valor da propriedade de conta especificada.
ms.openlocfilehash: 94134cee7886177ab840a6caff7d70d65bf9d4cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322250"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

Define o valor da propriedade de conta especificada.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parâmetros

_dwProp_
  
> no A marca de propriedade da propriedade Account a ser definida.
    
_pVar_
  
> no O valor da propriedade especificada.
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada do método foi bem-sucedida.  <br/> |
|E_INVALIDARG  <br/> |Uma marca de propriedade inválida foi especificada.  <br/> |
   
## <a name="remarks"></a>Comentários

Use [IOlkAccount:: SaveChanges](iolkaccount-savechanges.md) para salvar alterações no valor das propriedades da conta. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

