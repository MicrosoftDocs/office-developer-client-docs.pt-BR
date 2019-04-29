---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Exibe a caixa de diálogo Configurações da conta ou Adicionar nova conta.
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415030"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Exibe a caixa de diálogo **configurações da conta** ou **Adicionar nova conta** . 
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::DisplayAccountList ( 
    HWND hwnd,
    DWORD dwFlags,
    LPCWSTR wszTitle,
    DWORD cCategories,
    const CLSID * rgclsidCategories,
    const CLSID * pclsidType
);

```

## <a name="parameters"></a>Parâmetros

_hwnd_
  
> no O identificador para a janela à qual a caixa de diálogo exibida é modal. Pode ser zero.
    
_dwFlags_
  
> no Sinalizadores para modificar o comportamento da exibição. 
    
   - **ACCTUI_NO_WARNING**— não exibe o aviso de que as alterações não terão efeito até que o Outlook seja reiniciado. Aplica-se somente se o aplicativo estiver em execução no processo com o Outlook. exe.
    
   - **ACCTUI_SHOW_DATA_TAB**— mostrar a caixa de diálogo **configurações de conta** com a guia **dados** selecionada. Válido somente se **ACCTUI_SHOW_ACCTWIZARD** não estiver definido. 
    
   - **ACCTUI_SHOW_ACCTWIZARD**— exibe a caixa de diálogo **Adicionar nova conta** . 
    
_wszTitle_
  
> no Esse parâmetro não é usado e deve ser nulo.
    
_cCategories_
  
> no Este parâmetro não é usado e deve ser nulo. 
    
_rgclsidCategories_
  
> no Este parâmetro não é usado e deve ser nulo.
    
_pclsidType_
  
> no Este parâmetro não é usado e deve ser nulo.
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_ACCT_UI_BUSY  <br/> |Não foi possível criar a caixa de diálogo.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerente de contas não foi inicializado para uso.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |A caixa de diálogo **Adicionar nova conta** retornou um erro.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |O parâmetro _cCategories_, _rgclsidCategories_ou _pclsidType_ é não nulo.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |A caixa de diálogo **configurações da conta** retornou um erro.  <br/> |
   
## <a name="remarks"></a>Comentários

Os parâmetros _cCategories_, _rgclsidCategories_e _pclsidType_ não são usados neste momento e devem ser nulos.  _wszTitle_ não é usado e também deve ser nulo. 
  

