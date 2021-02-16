---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Modifica a ordem da categoria de contas especificada.
ms.openlocfilehash: 29dfe4fd1bda9e323481297167361650c3b3a173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422856"
---
# <a name="iolkaccountmanagersetorder"></a>IOlkAccountManager::SetOrder

Modifica a ordem da categoria de contas especificada.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a>Parâmetros

_pclsidCategory_
  
> [in] A ID de classe de categoria para a qual definir o pedido. O valor deve ser uma das seguintes opções:
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_cAccts_
  
> [in] O número de contas.
    
_rgAccts_
  
> [in] Uma matriz de IDs de conta. O tamanho da matriz é  _cAccts_.
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |A nova ordem de classificação tem um número diferente de contas que a ordem de classificação antiga.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais argumentos são inválidos.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerenciador de contas não foi inicializado para uso.  <br/> |
   
## <a name="remarks"></a>Comentários

O chamador aloca memória para  _prgAccts_ de ponteiro da matriz, bem como para a matriz na qual  _prgAccts_ aponta. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)  
- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

