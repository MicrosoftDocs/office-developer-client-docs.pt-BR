---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Obtém um enumerador para as contas da categoria ou tipo específico.
ms.openlocfilehash: d0d383dee0e76dd6310d01bd1482e307c2374856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423045"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a>IOlkAccountManager::EnumerateAccounts

Obtém um enumerador para as contas da categoria ou tipo específico.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a>Parâmetros

_pclsidCategory_
  
> no O identificador de classe da categoria a ser enumerada. O valor deve ser uma das seguintes opções:
    
   - CLSID_OlkMail 
    
   -  CLSID_OlkAddressBook 
    
   - CLSID_OlkStore 
    
_pclsidType_
  
> no O identificador de classe do tipo de conta a ser enumerado. O valor deve ser uma das seguintes opções:
    
   - CLSID_OlkPOP3Account
    
   - CLSID_OlkIMAP4Account
    
   - CLSID_OlkMAPIAccount
    
   - CLSID_OlkHotmailAccount
    
   - CLSID_OlkLDAPAccount
    
_dwFlags_
  
> [in] Sinalizadores para modificar o comportamento. O único valor com suporte é OLK_ACCOUNT_NO_FLAGS.
    
_ppEnum_
  
> bota Um enumerador que oferece suporte à interface [IOlkEnum](iolkenum.md) . 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerente de contas não foi inicializado para uso.  <br/> |
   
## <a name="remarks"></a>Comentários

Especificar NULL para Category retorna um enumerador de todas as contas do tipo especificado. Da mesma forma, especificar NULL para Type retorna um enumerador de todas as contas da categoria especificada.
  
 **IOlkAccountManager:: EnumerateAccounts** não dá suporte à categoria catálogo de endereços para uma conta do Exchange. Se a conta for uma conta do Exchange (*pclsidType* é **CLSID_OlkMAPIAccount** ) e você estiver tentando enumerar contas que implementam o catálogo de endereços (*prgclsidCategory* é **CLSID_OlkAddressBook** ), chamar ** IOlkAccountManager:: EnumerateAccounts** não retornará a conta do Exchange no enumerador de contas *ppEnum* . 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)  
- [IOlkEnum](iolkenum.md)

