---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Modifica a ordenação da categoria especificada das contas.
ms.openlocfilehash: fcb27404471c9b551320027b0ed6979926ad3d58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765964"
---
# <a name="iolkaccountmanagersetorder"></a>IOlkAccountManager::SetOrder

Modifica a ordenação da categoria especificada das contas.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a>Par�metros

_pclsidCategory_
  
> [in] A ID de classe de categoria para o qual definir a ordem. O valor deve ser uma das seguintes opções:
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_cAccts_
  
> [in] O número de contas.
    
_rgAccts_
  
> [in] Uma matriz de IDs de conta. O tamanho da matriz é _cAccts_.
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |Nova ordem de classificação tem um número diferente de contas que a ordem de classificação antigo.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais argumentos são inválidos.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerente de conta não foi inicializado para uso.  <br/> |
   
## <a name="remarks"></a>Coment�rios

O chamador aloca memória para o ponteiro de matriz _prgAccts_ , bem como para a matriz nos quais pontos _prgAccts_ . 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)  
- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

