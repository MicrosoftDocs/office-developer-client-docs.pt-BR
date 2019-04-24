---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Obtém as informações de tipo e categorias da conta especificada.
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318183"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

Obtém as informações de tipo e categorias da conta especificada.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>Parâmetros

_pclsidType_
  
> bota O identificador de classe para o tipo de conta. O valor deve ser uma das seguintes opções:
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> bota O número de categorias no _prgclsidCategory_.
    
_prgclsidCategory_
  
> bota Uma matriz de categorias à qual essa conta está associada. A matriz é do tamanho * _pcCategories_. O valor de cada categoria na matriz deve ser um dos seguintes:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Após o método retornar, você deve liberar *prgclsidCategory* usando [IOlkAccount:: freememory](iolkaccount-freememory.md).
  
**IOlkAccount:: GetAccountInfo** não dá suporte à categoria catálogo de endereços para uma conta do Exchange. Se a conta for uma conta do Exchange (*pclsidType* é **CLSID_OlkMAPIAccount** ) e a conta implementar o catálogo de endereços, chamar **IOlkAccount:: GetAccountInfo** não retornará **CLSID_OlkAddressBook** como uma categoria no * prgclsidCategory* . 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

