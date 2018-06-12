---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Obtém um enumerador para as contas do tipo ou categoria específica.
ms.openlocfilehash: f9b332c0bbc90b1a8f5f944492448055f23c0668
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765963"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a>IOlkAccountManager::EnumerateAccounts

Obtém um enumerador para as contas do tipo ou categoria específica.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a>Par�metros

_pclsidCategory_
  
> [in] O identificador de classe da categoria para enumerar. O valor deve ser uma das seguintes opções:
    
   - CLSID_OlkMail 
    
   -  CLSID_OlkAddressBook 
    
   - CLSID_OlkStore 
    
_pclsidType_
  
> [in] O identificador de classe do tipo de conta para enumerar. O valor deve ser uma das seguintes opções:
    
   - CLSID_OlkPOP3Account
    
   - CLSID_OlkIMAP4Account
    
   - CLSID_OlkMAPIAccount
    
   - CLSID_OlkHotmailAccount
    
   - CLSID_OlkLDAPAccount
    
_dwFlags_
  
> [in] Sinalizadores para modificar o comportamento. O único valor com suporte é OLK_ACCOUNT_NO_FLAGS.
    
_ppEnum_
  
> [out] Um enumerador que dá suporte à interface [IOlkEnum](iolkenum.md) . 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerente de conta não foi inicializado para uso.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Especificando NULL para categoria retorna um enumerador de todas as contas do tipo especificado. Da mesma forma, especificando NULL para tipo retorna um enumerador de todas as contas da categoria especificada.
  
 **IOlkAccountManager::EnumerateAccounts** não oferece suporte a categoria do catálogo de endereços para uma conta do Exchange. Se a conta for uma conta do Exchange (*pclsidType* é **CLSID_OlkMAPIAccount** ), e você está tentando enumerar contas que implementam o catálogo de endereços (*prgclsidCategory* é **CLSID_OlkAddressBook** ), chamar ** IOlkAccountManager::EnumerateAccounts** não retornará a conta do Exchange no enumerador de contas *ppEnum* . 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)  
- [IOlkEnum](iolkenum.md)

