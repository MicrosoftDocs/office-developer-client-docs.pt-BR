---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Notifica o cliente de alterações para a conta especificada.
ms.openlocfilehash: ea4cab8cb8571cf5f34637c08935c78c657e5503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765981"
---
# <a name="iolkaccountnotifynotify"></a>IOlkAccountNotify::Notify

Notifica o cliente de alterações para a conta especificada.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccountNotify](iolkaccountnotify.md).
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Par�metros

_dwNotify_
  
> [in] O tipo de notificação. O valor deve ser uma das seguintes opções:
    
   - NOTIFY_ACCT_CHANGED 
    
   - NOTIFY_ACCT_CREATED 
    
   - NOTIFY_ACCT_DELETED
    
   - NOTIFY_ACCT_ORDER_CHANGED 
    
   - NOTIFY_ACCT_PREDELETED 
    
 _dwAcctID_
  
> [in] A ID da conta da conta que tiver sido criada, alterado, excluído ou excluído anteriormente.
    
 _dwFlags_
  
>  [in] Não usado. OLK_ACCOUNT_NO_FLAGS é o único valor com suporte. 
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

