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
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321634"
---
# <a name="imapiformmgropenformcontainer"></a><span data-ttu-id="9123b-103">IMAPIFormMgr::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="9123b-103">IMAPIFormMgr::OpenFormContainer</span></span>

  
  
<span data-ttu-id="9123b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9123b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9123b-105">Abre uma [interface IMAPIFormContainer](imapiformcontaineriunknown.md) para um contêiner de formulário específico.</span><span class="sxs-lookup"><span data-stu-id="9123b-105">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span> 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="9123b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9123b-106">Parameters</span></span>

 <span data-ttu-id="9123b-107">_hfrmreg_</span><span class="sxs-lookup"><span data-stu-id="9123b-107">_hfrmreg_</span></span>
  
> <span data-ttu-id="9123b-108">[in] Uma enumeração HFRMREG que indica a biblioteca de formulário a ser aberta (ou seja, o contêiner de formulário a ser aberto).</span><span class="sxs-lookup"><span data-stu-id="9123b-108">[in] An HFRMREG enumeration that indicates the form library to open (that is, the form container to open).</span></span> <span data-ttu-id="9123b-109">Uma enumeração HFRMREG é uma enumeração específica de um provedor de biblioteca de formulário.</span><span class="sxs-lookup"><span data-stu-id="9123b-109">An HFRMREG enumeration is an enumeration that is specific to a form library provider.</span></span> <span data-ttu-id="9123b-110">Os valores de HFRMREG possíveis incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9123b-110">Possible HFRMREG values include the following:</span></span>
    
<span data-ttu-id="9123b-111">HFRMREG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="9123b-111">HFRMREG_DEFAULT</span></span> 
  
> <span data-ttu-id="9123b-112">Um contêiner de formulário conveniente.</span><span class="sxs-lookup"><span data-stu-id="9123b-112">A convenient form container.</span></span>
    
<span data-ttu-id="9123b-113">HFRMREG_FOLDER</span><span class="sxs-lookup"><span data-stu-id="9123b-113">HFRMREG_FOLDER</span></span> 
  
> <span data-ttu-id="9123b-114">Um contêiner de pasta.</span><span class="sxs-lookup"><span data-stu-id="9123b-114">A folder container.</span></span> 
    
<span data-ttu-id="9123b-115">HFRMREG_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="9123b-115">HFRMREG_PERSONAL</span></span> 
  
> <span data-ttu-id="9123b-116">O contêiner para o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="9123b-116">The container for the default message store.</span></span> 
    
<span data-ttu-id="9123b-117">HFRMREG_LOCAL</span><span class="sxs-lookup"><span data-stu-id="9123b-117">HFRMREG_LOCAL</span></span> 
  
> <span data-ttu-id="9123b-118">Um contêiner de formulário local.</span><span class="sxs-lookup"><span data-stu-id="9123b-118">A local form container.</span></span> 
    
 <span data-ttu-id="9123b-119">_lpunk_</span><span class="sxs-lookup"><span data-stu-id="9123b-119">_lpunk_</span></span>
  
> <span data-ttu-id="9123b-120">[in] Um ponteiro para o objeto para o qual a interface é aberta.</span><span class="sxs-lookup"><span data-stu-id="9123b-120">[in] A pointer to the object for which the interface is opened.</span></span> <span data-ttu-id="9123b-121">O  _parâmetro lpunk_ deve ser **nulo,** a menos que o valor do parâmetro  _hfrmreg_ exija um ponteiro de objeto.</span><span class="sxs-lookup"><span data-stu-id="9123b-121">The  _lpunk_ parameter must be **null** unless the value for the  _hfrmreg_ parameter requires an object pointer.</span></span> 
    
 <span data-ttu-id="9123b-122">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="9123b-122">_lppfcnt_</span></span>
  
> <span data-ttu-id="9123b-123">[out] Um ponteiro para um ponteiro para o objeto de contêiner de formulário retornado.</span><span class="sxs-lookup"><span data-stu-id="9123b-123">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9123b-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9123b-124">Return value</span></span>

<span data-ttu-id="9123b-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="9123b-125">S_OK</span></span> 
  
> <span data-ttu-id="9123b-126">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="9123b-126">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9123b-127">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="9123b-127">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="9123b-128">O objeto apontado por  _lpunk_ não dá suporte à interface necessária.</span><span class="sxs-lookup"><span data-stu-id="9123b-128">The object pointed to by  _lpunk_ does not support the required interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9123b-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="9123b-129">Remarks</span></span>

<span data-ttu-id="9123b-130">Visualizadores de formulário chamam o método **IMAPIFormMgr::OpenFormContainer** para abrir uma interface **IMAPIFormContainer** para um contêiner de formulário específico.</span><span class="sxs-lookup"><span data-stu-id="9123b-130">Form viewers call the **IMAPIFormMgr::OpenFormContainer** method to open an **IMAPIFormContainer** interface for a specific form container.</span></span> <span data-ttu-id="9123b-131">Essa interface pode então ser usada para instalar formulários e remover formulários de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="9123b-131">This interface can then be used for installing forms into and removing forms from a form container.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9123b-132">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9123b-132">Notes to callers</span></span>

<span data-ttu-id="9123b-133">Se o valor em _hfrmreg_ for HFRMREG_FOLDER, o identificador de interface  usado no _lpunk_ deverá ser não nulo e deverá permitir chamadas do método [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) para uma interface [IMAPIFolder.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="9123b-133">If the value in  _hfrmreg_ is HFRMREG_FOLDER, the interface identifier used in  _lpunk_ must be non- **null** and must allow [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method calls to an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
<span data-ttu-id="9123b-134">Para abrir o contêiner de formulário local, você deve usar uma chamada para o método **OpenFormContainer** ou a função [MAPIOpenLocalFormContainer;](mapiopenlocalformcontainer.md) você não pode usar o [método IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) para permitir que o usuário selecione o contêiner de formulário local.</span><span class="sxs-lookup"><span data-stu-id="9123b-134">To open the local form container, you must use a call to **OpenFormContainer** method or the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function; you cannot use the [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to enable the user to select the local form container.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9123b-135">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9123b-135">MFCMAPI reference</span></span>

<span data-ttu-id="9123b-136">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9123b-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9123b-137">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="9123b-137">**File**</span></span>|<span data-ttu-id="9123b-138">**Função**</span><span class="sxs-lookup"><span data-stu-id="9123b-138">**Function**</span></span>|<span data-ttu-id="9123b-139">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="9123b-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9123b-140">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9123b-140">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="9123b-141">CMainDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="9123b-141">CMainDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="9123b-142">MFCMAPI usa o **método IMAPIFormMgr::OpenFormContainer** para recuperar um contêiner de formulário para que o conteúdo do contêiner possa ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="9123b-142">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container so the container's contents can be rendered.</span></span>  <br/> |
|<span data-ttu-id="9123b-143">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9123b-143">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="9123b-144">CMsgStoreDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="9123b-144">CMsgStoreDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="9123b-145">MFCMAPI usa o método **IMAPIFormMgr::OpenFormContainer** para recuperar um contêiner de formulário para uma pasta para que o conteúdo do contêiner possa ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="9123b-145">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container for a folder so the container's contents can be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9123b-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="9123b-146">See also</span></span>



[<span data-ttu-id="9123b-147">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="9123b-147">IMAPIFormContainer::InstallForm</span></span>](imapiformcontainer-installform.md)
  
[<span data-ttu-id="9123b-148">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="9123b-148">IMAPIFormMgr::SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md)
  
[<span data-ttu-id="9123b-149">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="9123b-149">MAPIOpenLocalFormContainer</span></span>](mapiopenlocalformcontainer.md)
  
[<span data-ttu-id="9123b-150">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9123b-150">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="9123b-151">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="9123b-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

