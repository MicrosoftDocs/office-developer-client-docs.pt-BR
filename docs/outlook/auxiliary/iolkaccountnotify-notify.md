---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Notifica o cliente sobre as alterações na conta especificada.
ms.openlocfilehash: 269d8a8bd605c9d8a0a4057e87895522d8587ee9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321963"
---
# <a name="iolkaccountnotifynotify"></a>IOlkAccountNotify::Notify

Notifica o cliente sobre as alterações na conta especificada.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccountNotify](iolkaccountnotify.md).
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Parâmetros

_dwNotify_
  
> no O tipo de notificação. O valor deve ser uma das seguintes opções:
    
   - NOTIFY_ACCT_CHANGED 
    
   - NOTIFY_ACCT_CREATED 
    
   - NOTIFY_ACCT_DELETED
    
   - NOTIFY_ACCT_ORDER_CHANGED 
    
   - NOTIFY_ACCT_PREDELETED 
    
 _dwAcctID_
  
> no A ID da conta que foi criada, alterada, excluída ou excluída.
    
 _dwFlags_
  
>  no Não usado. OLK_ACCOUNT_NO_FLAGS é o único valor com suporte. 
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

