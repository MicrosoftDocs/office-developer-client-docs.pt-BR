---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Salva as alterações na conta especificada.
ms.openlocfilehash: dbb1dffa1725e96bd2ab635341718ce53738b864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322019"
---
# <a name="iolkaccountmanagersavechanges"></a>IOlkAccountManager::SaveChanges

Salva as alterações na conta especificada.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Parâmetros

_dwAcctID_
  
> no A ID da conta a ser salva. 
    
_dwFlags_
  
> [in] Sinalizadores para modificar o comportamento. OLK_ACCOUNT_NO_FLAGS é o único valor com suporte.
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada teve êxito  <br/> |
|E_ACCT_NOT_FOUND  <br/> |A conta especificada não pode ser encontrada.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerente de contas não foi inicializado para uso.  <br/> |
   
## <a name="remarks"></a>Comentários

Após alterar o valor das propriedades da conta usando [IOlkAccount:: SetProp](iolkaccount-setprop.md), use **IOlkAccountManager:: SaveChanges** ou [IOlkAccount::](iolkaccount-savechanges.md) SaveChanges para salvar essas alterações. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md) 
- [IOlkAccount::SaveChanges](iolkaccount-savechanges.md)

