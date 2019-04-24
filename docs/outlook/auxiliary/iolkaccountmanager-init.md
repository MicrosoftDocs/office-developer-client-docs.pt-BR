---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Inicializa o gerente de conta para uso.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322033"
---
# <a name="iolkaccountmanagerinit"></a>IOlkAccountManager::Init

Inicializa o gerente de conta para uso.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Parâmetros

_pAcctHelper_
  
> [em] Uma interface [IOlkAccountHelper](iolkaccounthelper.md)que fornece a funcionalidade de ajuda da conta. 
    
_dwFlags_
  
> [in] Sinalizadores para modificar o comportamento.
    
   - **ACCT_INIT_NO_STORES_CHECK**, impede que uma conta (como uma conta IMAP) seja sincronizada com um repositório associado. 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS**, impede que os serviços MAPI sejam sincronizados com as contas. 
   
   - **ACCT_INIT_NO_NOTIFICATIONS**, impede que o Gerente de Contas intercepte a transmissão de mensagens destinadas a outros aplicativos. 
   
   - **OLK_ACCOUNT_NO_FLAGS**, sincroniza os serviços MAPI com as contas. 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |**Init** já foi chamado.  <br/> |
|E_OLK_REGISTRY  <br/> |O gerente de conta não pôde acessar as configurações de registro necessárias.  <br/> |
   
## <a name="remarks"></a>Comentários

O cliente deverá ligar **IOlkAccountManager::Init** para inicializar o gerente de conta antes de usar o gerenciador de conta para acessar contas ou configurar notificações. Como o Outlook sincroniza automaticamente serviços MAPI com contas na inicialização, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** a menos que haja uma causa específica para sincronizar. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)

