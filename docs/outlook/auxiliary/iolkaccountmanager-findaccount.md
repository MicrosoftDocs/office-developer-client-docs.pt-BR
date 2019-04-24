---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Localiza uma conta por valor de propriedade.
ms.openlocfilehash: d09bce88413f85ee3ccc332c3cb88bb545a0ccaf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322075"
---
# <a name="iolkaccountmanagerfindaccount"></a>IOlkAccountManager::FindAccount

Localiza uma conta por valor de propriedade.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a>Parâmetros

_dwProp_
  
> no A propriedade a ser pesquisada. Deve ser [PROP_ACCT_ID](prop_acct_id.md) ou [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).
    
_pVar_
  
> no O valor a ser correspondido.
    
_ppAccount_
  
> bota A conta encontrada. Este objeto oferece suporte a uma interface [IOlkAccount](iolkaccount.md) . 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |A conta especificada não pode ser encontrada.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerente de contas não foi inicializado para uso.  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
   
## <a name="see-also"></a>Confira também

- [ACCT_VARIANT](acct_variant.md)  
- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

