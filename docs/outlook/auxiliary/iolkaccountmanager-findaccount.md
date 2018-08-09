---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Localiza uma conta pelo valor da propriedade.
ms.openlocfilehash: a7d016ab7e265e547b33940c16f96979bd5fa87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765961"
---
# <a name="iolkaccountmanagerfindaccount"></a>IOlkAccountManager::FindAccount

Localiza uma conta pelo valor da propriedade.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a>Parâmetros

_dwProp_
  
> [in] A propriedade de pesquisar. Deve ser [PROP_ACCT_ID](prop_acct_id.md) ou [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).
    
_pVar_
  
> [in] O valor a ser correspondido.
    
_ppAccount_
  
> [out] A conta foi encontrada. Este objeto oferece suporte a uma interface [IOlkAccount](iolkaccount.md) . 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |A conta especificada não foi encontrada.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerente de conta não foi inicializado para uso.  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
   
## <a name="see-also"></a>Confira também

- [ACCT_VARIANT](acct_variant.md)  
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

