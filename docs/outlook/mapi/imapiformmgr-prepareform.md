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
ms.openlocfilehash: 6e8ea7230ae86dee99cc4413715055fc53afa900
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579722"
---
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="741bd-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="741bd-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="741bd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="741bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="741bd-105">Baixa um formulário para abertura.</span><span class="sxs-lookup"><span data-stu-id="741bd-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="741bd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="741bd-106">Parameters</span></span>

 <span data-ttu-id="741bd-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="741bd-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="741bd-108">[in] Um identificador para a janela pai do indicador de progresso é exibida enquanto o formulário é baixado.</span><span class="sxs-lookup"><span data-stu-id="741bd-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="741bd-109">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MAPI_DIALOG é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="741bd-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="741bd-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="741bd-110">_ulFlags_</span></span>
  
> <span data-ttu-id="741bd-111">[in] Uma bitmask dos sinalizadores que controla como o formulário é baixado.</span><span class="sxs-lookup"><span data-stu-id="741bd-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="741bd-112">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="741bd-112">The following flag can be set:</span></span>
    
<span data-ttu-id="741bd-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="741bd-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="741bd-114">Exibe uma interface de usuário para fornecer status ou solicita ao usuário para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="741bd-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="741bd-115">Se esse sinalizador não estiver definida, nenhuma interface de usuário é exibida.</span><span class="sxs-lookup"><span data-stu-id="741bd-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="741bd-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="741bd-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="741bd-117">[in] Um ponteiro para um objeto de informações de formulário para o formulário sejam baixados.</span><span class="sxs-lookup"><span data-stu-id="741bd-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="741bd-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="741bd-118">Return value</span></span>

<span data-ttu-id="741bd-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="741bd-119">S_OK</span></span> 
  
> <span data-ttu-id="741bd-120">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="741bd-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="741bd-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="741bd-121">Remarks</span></span>

<span data-ttu-id="741bd-122">Visualizadores de formulário chame o método de **IMAPIFormMgr::PrepareForm** para baixar um formulário a partir de um contêiner de formulário para abertura.</span><span class="sxs-lookup"><span data-stu-id="741bd-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="741bd-123">A maioria dos visualizadores de formulário não é necessário chamar **PrepareForm**, pois métodos [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) tanto o [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) chamam **PrepareForm**, se necessário.</span><span class="sxs-lookup"><span data-stu-id="741bd-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="741bd-124">Você pode usar **PrepareForm** para obter as bibliotecas de vínculos dinâmicos (DLLs) e outros arquivos associados a um formulário para modificá-los.</span><span class="sxs-lookup"><span data-stu-id="741bd-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="741bd-125">Se o formulário modificado for carregado de volta para seu contêiner de formulário, ele deve ser reinstalado.</span><span class="sxs-lookup"><span data-stu-id="741bd-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="741bd-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="741bd-126">See also</span></span>



[<span data-ttu-id="741bd-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="741bd-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="741bd-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="741bd-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="741bd-129">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="741bd-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

