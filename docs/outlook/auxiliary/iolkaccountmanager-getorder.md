---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Obtém a ordenação da categoria de contas especificada.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424620"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

Obtém a ordenação da categoria de contas especificada.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccountManager](iolkaccountmanager.md)
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a>Parâmetros

_pclsidCategory_
  
> no A ID de classe de categoria para a qual obter o pedido. O valor deve ser uma das seguintes opções:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_pcAccts_
  
>  bota O número de contas. 
    
_prgAccts_
  
> bota Um ponteiro para uma matriz de contas.
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada teve êxito  <br/> |
|E_INVALIDARG  <br/> |Um ou mais argumentos são inválidos.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerente de contas não foi inicializado para uso.  <br/> |
   
## <a name="remarks"></a>Comentários

Antes de chamar esse método, o chamador aloca apenas um ponteiro de matriz *prgAccts* , mas não há memória para a matriz na qual *prgAccts* aponta. Após o método retornar, o chamador deverá usar [IOlkAccountManager:: freememory](iolkaccountmanager-freememory.md) para liberar a memória alocada para o *prgAccts* . 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)

