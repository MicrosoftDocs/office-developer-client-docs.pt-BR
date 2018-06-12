---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Cancela o registro de um cliente com o Gerenciador de contas para notificações para todas as contas.
ms.openlocfilehash: 0632bc6bd98e218cf323262ea480b020185438f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765970"
---
# <a name="iolkaccountmanagerunadvise"></a>IOlkAccountManager::Unadvise

Cancela o registro de um cliente com o Gerenciador de contas para notificações para todas as contas. 
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a>Par�metros

_dwCookie_
  
> [in] O cookie retornado por [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais argumentos são inválidos.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerente de conta não foi inicializado para uso.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)  
- [IOlkAccountManager::Advise](iolkaccountmanager-advise.md)

