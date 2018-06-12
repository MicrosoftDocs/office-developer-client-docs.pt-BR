---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Confirma as alterações para o objeto account escrevendo no repositório de registro.
ms.openlocfilehash: ebff8af8af8a7512b577b36a2c31f76f3297a19d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765906"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

Confirma as alterações para o objeto account escrevendo no repositório de registro.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Par�metros

_dwFlags_
  
> [in] Sinalizadores para modificar o comportamento. OLK_ACCOUNT_NO_FLAGS é o único valor com suporte.
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |O método foi bem-sucedida.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Não é possível localizar a conta especificada.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerente de conta não foi inicializado para uso.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Após alterar o valor das propriedades de conta usando [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** salve as alterações. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

