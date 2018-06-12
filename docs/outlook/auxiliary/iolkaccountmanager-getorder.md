---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Obtém a ordenação da categoria especificada das contas.
ms.openlocfilehash: d05e354e25d49a51b3d3f8f053c2b39dc37b333f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765968"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

Obtém a ordenação da categoria especificada das contas.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccountManager](iolkaccountmanager.md)
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a>Par�metros

_pclsidCategory_
  
> [in] A ID de classe de categoria para o qual deseja obter a ordem. O valor deve ser uma das seguintes opções:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_pcAccts_
  
>  [out] O número de contas. 
    
_prgAccts_
  
> [out] Um ponteiro para uma matriz de contas.
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida  <br/> |
|E_INVALIDARG  <br/> |Um ou mais argumentos são inválidos.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerente de conta não foi inicializado para uso.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Antes de chamar este método, o chamador aloca apenas uma matriz ponteiro *prgAccts* , mas não há memória para a matriz nos quais pontos *prgAccts* . Depois que esse método retorna, o chamador deve usar [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) para liberar a memória alocada para *prgAccts* . 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)

