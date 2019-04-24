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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322061"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="98b07-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="98b07-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="98b07-104">Exibe a caixa de diálogo **configurações da conta** ou **Adicionar nova conta** .</span><span class="sxs-lookup"><span data-stu-id="98b07-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="98b07-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="98b07-105">Quick info</span></span>

<span data-ttu-id="98b07-106">Confira [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="98b07-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="98b07-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98b07-107">Parameters</span></span>

<span data-ttu-id="98b07-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="98b07-108">_hwnd_</span></span>
  
> <span data-ttu-id="98b07-109">no O identificador para a janela à qual a caixa de diálogo exibida é modal.</span><span class="sxs-lookup"><span data-stu-id="98b07-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="98b07-110">Pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="98b07-110">May be zero.</span></span>
    
<span data-ttu-id="98b07-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="98b07-111">_dwFlags_</span></span>
  
> <span data-ttu-id="98b07-112">no Sinalizadores para modificar o comportamento da exibição.</span><span class="sxs-lookup"><span data-stu-id="98b07-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="98b07-113">**ACCTUI_NO_WARNING**— não exibe o aviso de que as alterações não terão efeito até que o Outlook seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="98b07-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="98b07-114">Aplica-se somente se o aplicativo estiver em execução no processo com o Outlook. exe.</span><span class="sxs-lookup"><span data-stu-id="98b07-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="98b07-115">**ACCTUI_SHOW_DATA_TAB**— mostrar a caixa de diálogo **configurações de conta** com a guia **dados** selecionada.</span><span class="sxs-lookup"><span data-stu-id="98b07-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="98b07-116">Válido somente se **ACCTUI_SHOW_ACCTWIZARD** não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="98b07-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="98b07-117">**ACCTUI_SHOW_ACCTWIZARD**— exibe a caixa de diálogo **Adicionar nova conta** .</span><span class="sxs-lookup"><span data-stu-id="98b07-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="98b07-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="98b07-118">_wszTitle_</span></span>
  
> <span data-ttu-id="98b07-119">no Esse parâmetro não é usado e deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="98b07-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="98b07-120">_cCategories_</span><span class="sxs-lookup"><span data-stu-id="98b07-120">_cCategories_</span></span>
  
> <span data-ttu-id="98b07-121">no Este parâmetro não é usado e deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="98b07-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="98b07-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="98b07-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="98b07-123">no Este parâmetro não é usado e deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="98b07-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="98b07-124">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="98b07-124">_pclsidType_</span></span>
  
> <span data-ttu-id="98b07-125">no Este parâmetro não é usado e deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="98b07-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="98b07-126">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="98b07-126">Return values</span></span>

|<span data-ttu-id="98b07-127">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="98b07-127">**HRESULT**</span></span>|<span data-ttu-id="98b07-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="98b07-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98b07-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="98b07-129">S_OK</span></span>  <br/> |<span data-ttu-id="98b07-130">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="98b07-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="98b07-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="98b07-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="98b07-132">Não foi possível criar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="98b07-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="98b07-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="98b07-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="98b07-134">O gerente de contas não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="98b07-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="98b07-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="98b07-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="98b07-136">A caixa de diálogo **Adicionar nova conta** retornou um erro.</span><span class="sxs-lookup"><span data-stu-id="98b07-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="98b07-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="98b07-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="98b07-138">O parâmetro _cCategories_, _rgclsidCategories_ou _pclsidType_ é não nulo.</span><span class="sxs-lookup"><span data-stu-id="98b07-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="98b07-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="98b07-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="98b07-140">A caixa de diálogo **configurações da conta** retornou um erro.</span><span class="sxs-lookup"><span data-stu-id="98b07-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98b07-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="98b07-141">Remarks</span></span>

<span data-ttu-id="98b07-142">Os parâmetros _cCategories_, _rgclsidCategories_e _pclsidType_ não são usados neste momento e devem ser nulos.</span><span class="sxs-lookup"><span data-stu-id="98b07-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="98b07-143">_wszTitle_ não é usado e também deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="98b07-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

