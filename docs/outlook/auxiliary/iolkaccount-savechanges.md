---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Confirma as alterações no objeto Account gravando no repositório do registro.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425831"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

Confirma as alterações no objeto Account gravando no repositório do registro.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Parâmetros

_dwFlags_
  
> [in] Sinalizadores para modificar o comportamento. OLK_ACCOUNT_NO_FLAGS é o único valor com suporte.
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |O método foi bem-sucedido.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Não é possível localizar a conta especificada.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerente de contas não foi inicializado para uso.  <br/> |
   
## <a name="remarks"></a>Comentários

Após alterar o valor das propriedades da conta usando [IOlkAccount:: SetProp](iolkaccount-setprop.md), use **IOlkAccount:: SaveChanges** para salvar essas alterações. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

