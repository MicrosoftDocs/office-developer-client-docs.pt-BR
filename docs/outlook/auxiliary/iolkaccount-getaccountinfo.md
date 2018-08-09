---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Obtém as informações de tipo e categorias para a conta especificada.
ms.openlocfilehash: 85f27d1d5f47a372090b208821b52656a56559ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765891"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

Obtém as informações de tipo e categorias para a conta especificada.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>Parâmetros

_pclsidType_
  
> [out] O identificador de classe do tipo de conta. O valor deve ser uma das seguintes opções:
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> [out] O número de categorias no _prgclsidCategory_.
    
_prgclsidCategory_
  
> [out] Uma matriz das categorias que essa conta está associada. A matriz é do tamanho * _pcCategories_. O valor de cada categoria na matriz deve ser um destes procedimentos:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Depois que esse método retorna, você deve liberar *prgclsidCategory* usando [IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
**IOlkAccount::GetAccountInfo** não oferece suporte a categoria do catálogo de endereços para uma conta do Exchange. Se a conta for uma troca conta (*pclsidType* é **CLSID_OlkMAPIAccount** ) e a conta implementa o catálogo de endereços, chamada **IOlkAccount::GetAccountInfo** não retornará **CLSID_OlkAddressBook** como uma categoria no * prgclsidCategory* . 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

