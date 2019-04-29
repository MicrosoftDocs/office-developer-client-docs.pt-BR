---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d0d5d8fe13a3c192dc0b0a8ddc0f5f945fa16f15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416647"
---
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="d499c-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="d499c-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="d499c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d499c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d499c-105">Baixa um formulário para abertura.</span><span class="sxs-lookup"><span data-stu-id="d499c-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="d499c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d499c-106">Parameters</span></span>

 <span data-ttu-id="d499c-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d499c-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d499c-108">no Uma alça para a janela pai do indicador de progresso que é exibida enquanto o formulário é baixado.</span><span class="sxs-lookup"><span data-stu-id="d499c-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="d499c-109">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MAPI_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="d499c-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="d499c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d499c-110">_ulFlags_</span></span>
  
> <span data-ttu-id="d499c-111">no Uma bitmask de sinalizadores que controla como o formulário é baixado.</span><span class="sxs-lookup"><span data-stu-id="d499c-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="d499c-112">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="d499c-112">The following flag can be set:</span></span>
    
<span data-ttu-id="d499c-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="d499c-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="d499c-114">Exibe uma interface do usuário para fornecer status ou solicitar mais informações ao usuário.</span><span class="sxs-lookup"><span data-stu-id="d499c-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="d499c-115">Se esse sinalizador não for definido, nenhuma interface de usuário será exibida.</span><span class="sxs-lookup"><span data-stu-id="d499c-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="d499c-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="d499c-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="d499c-117">no Um ponteiro para um objeto de informações de formulário para o formulário ser baixado.</span><span class="sxs-lookup"><span data-stu-id="d499c-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d499c-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d499c-118">Return value</span></span>

<span data-ttu-id="d499c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d499c-119">S_OK</span></span> 
  
> <span data-ttu-id="d499c-120">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="d499c-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d499c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d499c-121">Remarks</span></span>

<span data-ttu-id="d499c-122">Os visualizadores de formulários chamam o método **IMAPIFormMgr::P repareform** para baixar um formulário de um contêiner de formulários para abertura.</span><span class="sxs-lookup"><span data-stu-id="d499c-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="d499c-123">A maioria dos visualizadores de formulário não precisa chamar **PrepareForm**, porque os métodos [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) e [IMAPIFormMgr:: loadform](imapiformmgr-loadform.md) chamam **PrepareForm**, se necessário.</span><span class="sxs-lookup"><span data-stu-id="d499c-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="d499c-124">Você pode usar o **PrepareForm** para obter as bibliotecas de vínculo dinâmico (DLLs) e outros arquivos associados a um formulário para modificá-los.</span><span class="sxs-lookup"><span data-stu-id="d499c-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="d499c-125">Se o formulário modificado for carregado de volta para o contêiner de formulários, ele deverá ser reinstalado.</span><span class="sxs-lookup"><span data-stu-id="d499c-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d499c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d499c-126">See also</span></span>



[<span data-ttu-id="d499c-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="d499c-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="d499c-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="d499c-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="d499c-129">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d499c-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

