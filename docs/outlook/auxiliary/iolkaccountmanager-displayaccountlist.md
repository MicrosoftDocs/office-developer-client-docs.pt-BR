---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Exibe a caixa de diálogo as configurações de conta ou adicionar nova conta.
ms.openlocfilehash: 3c7c433eb4d8f316d32b6cd12bbbbb0e1a1cee43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765967"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Exibe a caixa de diálogo as **Configurações de conta** ou **Adicionar nova conta** . 
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccountManager](iolkaccountmanager.md).
  
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

## <a name="parameters"></a>Par�metros

_hwnd_
  
> [in] O identificador para a janela para o qual a caixa de diálogo exibida é modal. Pode ser zero.
    
_dwFlags_
  
> [in] Sinalizadores para modificar o comportamento da tela. 
    
   - **ACCTUI_NO_WARNING**— não exibe o aviso de que as alterações não entrarão em vigor até que o Outlook seja reiniciado. Aplica-se apenas se o aplicativo está em execução em processo com Outlook.exe.
    
   - **ACCTUI_SHOW_DATA_TAB**— exibe a caixa de diálogo de **Configurações de conta** com a guia de **dados** selecionada. É válido somente se **ACCTUI_SHOW_ACCTWIZARD** não estiver definida. 
    
   - **ACCTUI_SHOW_ACCTWIZARD**— exibir a caixa de diálogo **Adicionar nova conta** . 
    
_wszTitle_
  
> [in] Este parâmetro não for usado e deve ser NULL.
    
_cCategories_
  
> [in] Este parâmetro não for usado e deve ser NULL. 
    
_rgclsidCategories_
  
> [in] Este parâmetro não for usado e deve ser NULL.
    
_pclsidType_
  
> [in] Este parâmetro não for usado e deve ser NULL.
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_ACCT_UI_BUSY  <br/> |A caixa de diálogo não pôde ser criada.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |O gerente de conta não foi inicializado para uso.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |A caixa de diálogo **Adicionar nova conta** retornou um erro.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |O parâmetro _cCategories_, _rgclsidCategories_ou _pclsidType_ é não-nulos.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |A caixa de diálogo **Configurações de conta** retornou um erro.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Os parâmetros _cCategories_, _rgclsidCategories_e _pclsidType_ não são usados neste momento e devem ser NULL.  _wszTitle_ não é usado e também deve ser NULL. 
  

