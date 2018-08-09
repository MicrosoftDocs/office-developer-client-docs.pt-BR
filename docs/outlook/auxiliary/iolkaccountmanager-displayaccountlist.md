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
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="e19e6-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="e19e6-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="e19e6-104">Exibe a caixa de diálogo as **Configurações de conta** ou **Adicionar nova conta** .</span><span class="sxs-lookup"><span data-stu-id="e19e6-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e19e6-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="e19e6-105">Quick info</span></span>

<span data-ttu-id="e19e6-106">Consulte [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="e19e6-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="e19e6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e19e6-107">Parameters</span></span>

<span data-ttu-id="e19e6-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="e19e6-108">_hwnd_</span></span>
  
> <span data-ttu-id="e19e6-109">[in] O identificador para a janela para o qual a caixa de diálogo exibida é modal.</span><span class="sxs-lookup"><span data-stu-id="e19e6-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="e19e6-110">Pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="e19e6-110">May be zero.</span></span>
    
<span data-ttu-id="e19e6-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="e19e6-111">_dwFlags_</span></span>
  
> <span data-ttu-id="e19e6-112">[in] Sinalizadores para modificar o comportamento da tela.</span><span class="sxs-lookup"><span data-stu-id="e19e6-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="e19e6-113">**ACCTUI_NO_WARNING**— não exibe o aviso de que as alterações não entrarão em vigor até que o Outlook seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="e19e6-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="e19e6-114">Aplica-se apenas se o aplicativo está em execução em processo com Outlook.exe.</span><span class="sxs-lookup"><span data-stu-id="e19e6-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="e19e6-115">**ACCTUI_SHOW_DATA_TAB**— exibe a caixa de diálogo de **Configurações de conta** com a guia de **dados** selecionada.</span><span class="sxs-lookup"><span data-stu-id="e19e6-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="e19e6-116">É válido somente se **ACCTUI_SHOW_ACCTWIZARD** não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="e19e6-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="e19e6-117">**ACCTUI_SHOW_ACCTWIZARD**— exibir a caixa de diálogo **Adicionar nova conta** .</span><span class="sxs-lookup"><span data-stu-id="e19e6-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="e19e6-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="e19e6-118">_wszTitle_</span></span>
  
> <span data-ttu-id="e19e6-119">[in] Este parâmetro não for usado e deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="e19e6-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="e19e6-120">_cCategories_</span><span class="sxs-lookup"><span data-stu-id="e19e6-120">_cCategories_</span></span>
  
> <span data-ttu-id="e19e6-121">[in] Este parâmetro não for usado e deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="e19e6-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="e19e6-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="e19e6-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="e19e6-123">[in] Este parâmetro não for usado e deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="e19e6-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="e19e6-124">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="e19e6-124">_pclsidType_</span></span>
  
> <span data-ttu-id="e19e6-125">[in] Este parâmetro não for usado e deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="e19e6-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e19e6-126">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="e19e6-126">Return values</span></span>

|<span data-ttu-id="e19e6-127">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e19e6-127">**HRESULT**</span></span>|<span data-ttu-id="e19e6-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e19e6-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e19e6-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="e19e6-129">S_OK</span></span>  <br/> |<span data-ttu-id="e19e6-130">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e19e6-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="e19e6-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="e19e6-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="e19e6-132">A caixa de diálogo não pôde ser criada.</span><span class="sxs-lookup"><span data-stu-id="e19e6-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="e19e6-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e19e6-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="e19e6-134">O gerente de conta não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="e19e6-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="e19e6-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="e19e6-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="e19e6-136">A caixa de diálogo **Adicionar nova conta** retornou um erro.</span><span class="sxs-lookup"><span data-stu-id="e19e6-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="e19e6-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e19e6-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="e19e6-138">O parâmetro _cCategories_, _rgclsidCategories_ou _pclsidType_ é não-nulos.</span><span class="sxs-lookup"><span data-stu-id="e19e6-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="e19e6-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="e19e6-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="e19e6-140">A caixa de diálogo **Configurações de conta** retornou um erro.</span><span class="sxs-lookup"><span data-stu-id="e19e6-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e19e6-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="e19e6-141">Remarks</span></span>

<span data-ttu-id="e19e6-142">Os parâmetros _cCategories_, _rgclsidCategories_e _pclsidType_ não são usados neste momento e devem ser NULL.</span><span class="sxs-lookup"><span data-stu-id="e19e6-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="e19e6-143">_wszTitle_ não é usado e também deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="e19e6-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

