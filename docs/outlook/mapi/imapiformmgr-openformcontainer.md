---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4bf3d9159dd1ed31fb93569218770f1015579339
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582921"
---
# <a name="imapiformmgropenformcontainer"></a><span data-ttu-id="b800e-103">IMAPIFormMgr::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="b800e-103">IMAPIFormMgr::OpenFormContainer</span></span>

  
  
<span data-ttu-id="b800e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b800e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b800e-105">Abre uma interface [IMAPIFormContainer](imapiformcontaineriunknown.md) para um contêiner de formulário específico.</span><span class="sxs-lookup"><span data-stu-id="b800e-105">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span> 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="b800e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b800e-106">Parameters</span></span>

 <span data-ttu-id="b800e-107">_hfrmreg_</span><span class="sxs-lookup"><span data-stu-id="b800e-107">_hfrmreg_</span></span>
  
> <span data-ttu-id="b800e-108">[in] Uma enumeração HFRMREG que indica a biblioteca de formulários para abrir (ou seja, o contêiner de formulário para abrir).</span><span class="sxs-lookup"><span data-stu-id="b800e-108">[in] An HFRMREG enumeration that indicates the form library to open (that is, the form container to open).</span></span> <span data-ttu-id="b800e-109">Uma enumeração de HFRMREG é uma enumeração que é específica para um provedor de biblioteca de formulário.</span><span class="sxs-lookup"><span data-stu-id="b800e-109">An HFRMREG enumeration is an enumeration that is specific to a form library provider.</span></span> <span data-ttu-id="b800e-110">Os valores possíveis HFRMREG incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b800e-110">Possible HFRMREG values include the following:</span></span>
    
<span data-ttu-id="b800e-111">HFRMREG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="b800e-111">HFRMREG_DEFAULT</span></span> 
  
> <span data-ttu-id="b800e-112">Um contêiner de forma conveniente.</span><span class="sxs-lookup"><span data-stu-id="b800e-112">A convenient form container.</span></span>
    
<span data-ttu-id="b800e-113">HFRMREG_FOLDER</span><span class="sxs-lookup"><span data-stu-id="b800e-113">HFRMREG_FOLDER</span></span> 
  
> <span data-ttu-id="b800e-114">Um contêiner de pasta.</span><span class="sxs-lookup"><span data-stu-id="b800e-114">A folder container.</span></span> 
    
<span data-ttu-id="b800e-115">HFRMREG_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="b800e-115">HFRMREG_PERSONAL</span></span> 
  
> <span data-ttu-id="b800e-116">O contêiner para o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="b800e-116">The container for the default message store.</span></span> 
    
<span data-ttu-id="b800e-117">HFRMREG_LOCAL</span><span class="sxs-lookup"><span data-stu-id="b800e-117">HFRMREG_LOCAL</span></span> 
  
> <span data-ttu-id="b800e-118">Um contêiner de local do formulário.</span><span class="sxs-lookup"><span data-stu-id="b800e-118">A local form container.</span></span> 
    
 <span data-ttu-id="b800e-119">_lpunk_</span><span class="sxs-lookup"><span data-stu-id="b800e-119">_lpunk_</span></span>
  
> <span data-ttu-id="b800e-120">[in] Um ponteiro para o objeto para o qual a interface é aberta.</span><span class="sxs-lookup"><span data-stu-id="b800e-120">[in] A pointer to the object for which the interface is opened.</span></span> <span data-ttu-id="b800e-121">O parâmetro _lpunk_ deve ser **Nulo** , a menos que o valor do parâmetro _hfrmreg_ requer um ponteiro de objeto.</span><span class="sxs-lookup"><span data-stu-id="b800e-121">The  _lpunk_ parameter must be **null** unless the value for the  _hfrmreg_ parameter requires an object pointer.</span></span> 
    
 <span data-ttu-id="b800e-122">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="b800e-122">_lppfcnt_</span></span>
  
> <span data-ttu-id="b800e-123">[out] Um ponteiro para um ponteiro para o objeto de contêiner do formulário retornado.</span><span class="sxs-lookup"><span data-stu-id="b800e-123">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b800e-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b800e-124">Return value</span></span>

<span data-ttu-id="b800e-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="b800e-125">S_OK</span></span> 
  
> <span data-ttu-id="b800e-126">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="b800e-126">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b800e-127">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="b800e-127">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="b800e-128">O objeto apontado pela _lpunk_ não suporta a interface necessária.</span><span class="sxs-lookup"><span data-stu-id="b800e-128">The object pointed to by  _lpunk_ does not support the required interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b800e-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="b800e-129">Remarks</span></span>

<span data-ttu-id="b800e-130">Visualizadores de formulário chame o método de **IMAPIFormMgr::OpenFormContainer** para abrir uma interface **IMAPIFormContainer** para um contêiner de formulário específico.</span><span class="sxs-lookup"><span data-stu-id="b800e-130">Form viewers call the **IMAPIFormMgr::OpenFormContainer** method to open an **IMAPIFormContainer** interface for a specific form container.</span></span> <span data-ttu-id="b800e-131">Essa interface, em seguida, pode ser usado para instalar em e remoção de formulários do contêiner de um formulário.</span><span class="sxs-lookup"><span data-stu-id="b800e-131">This interface can then be used for installing forms into and removing forms from a form container.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b800e-132">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="b800e-132">Notes to callers</span></span>

<span data-ttu-id="b800e-133">Se o valor em _hfrmreg_ for HFRMREG_FOLDER, o identificador de interface usado em _lpunk_ deve ser não - **Nulo** e deve permitir chamadas de métodos [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) para uma interface [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="b800e-133">If the value in  _hfrmreg_ is HFRMREG_FOLDER, the interface identifier used in  _lpunk_ must be non- **null** and must allow [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) method calls to an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
<span data-ttu-id="b800e-134">Para abrir o contêiner de formulário local, você deve usar uma chamada ao método **OpenFormContainer** ou a função [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) ; Você não pode usar o método de [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) para permitir que o usuário selecionar o contêiner de local do formulário.</span><span class="sxs-lookup"><span data-stu-id="b800e-134">To open the local form container, you must use a call to **OpenFormContainer** method or the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function; you cannot use the [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to enable the user to select the local form container.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b800e-135">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b800e-135">MFCMAPI reference</span></span>

<span data-ttu-id="b800e-136">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b800e-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b800e-137">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b800e-137">**File**</span></span>|<span data-ttu-id="b800e-138">**Function**</span><span class="sxs-lookup"><span data-stu-id="b800e-138">**Function**</span></span>|<span data-ttu-id="b800e-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b800e-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b800e-140">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b800e-140">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="b800e-141">CMainDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="b800e-141">CMainDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="b800e-142">MFCMAPI usa o método **IMAPIFormMgr::OpenFormContainer** para recuperar um contêiner de formulário para que o conteúdo do contêiner pode ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="b800e-142">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container so the container's contents can be rendered.</span></span>  <br/> |
|<span data-ttu-id="b800e-143">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b800e-143">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="b800e-144">CMsgStoreDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="b800e-144">CMsgStoreDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="b800e-145">MFCMAPI usa o método **IMAPIFormMgr::OpenFormContainer** para recuperar um contêiner de formulário para uma pasta, para que o conteúdo do contêiner pode ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="b800e-145">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container for a folder so the container's contents can be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b800e-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="b800e-146">See also</span></span>



[<span data-ttu-id="b800e-147">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="b800e-147">IMAPIFormContainer::InstallForm</span></span>](imapiformcontainer-installform.md)
  
[<span data-ttu-id="b800e-148">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="b800e-148">IMAPIFormMgr::SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md)
  
[<span data-ttu-id="b800e-149">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="b800e-149">MAPIOpenLocalFormContainer</span></span>](mapiopenlocalformcontainer.md)
  
[<span data-ttu-id="b800e-150">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b800e-150">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="b800e-151">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b800e-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

