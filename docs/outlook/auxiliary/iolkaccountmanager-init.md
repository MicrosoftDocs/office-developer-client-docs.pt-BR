---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Inicializa o gerente de conta para uso.
ms.openlocfilehash: 621c6a73ab2bcbdff17b87ce15af8b4e0c2e1e24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765958"
---
# <a name="iolkaccountmanagerinit"></a>IOlkAccountManager::Init

Inicializa o gerente de conta para uso.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Parâmetros

_pAcctHelper_
  
> [in] Uma interface [IOlkAccountHelper](iolkaccounthelper.md) que fornece a funcionalidade de auxiliar de conta. 
    
_dwFlags_
  
> [in] Sinalizadores para modificar o comportamento.
    
   - **ACCT_INIT_NO_STORES_CHECK** — evita a sincronização com um repositório associado de uma conta (por exemplo, uma conta IMAP). 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS** — serviços MAPI impede da sincronização com contas. 
    
   - **OLK_ACCOUNT_NO_FLAGS** — serviços MAPI sincroniza com contas. 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |**Inicialização** já foi chamado.  <br/> |
|E_OLK_REGISTRY  <br/> |O gerente de conta não foi possível acessar as configurações do registro necessárias.  <br/> |
   
## <a name="remarks"></a>Comentários

O cliente deve chamar **IOlkAccountManager::Init** para inicializar a conta do gerente antes de usar o Gerenciador de conta para contas de acessar ou configurar as notificações. Como o Outlook sincroniza automaticamente serviços MAPI com contas na inicialização, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** , a menos que haja uma causa específica para sincronizar. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

