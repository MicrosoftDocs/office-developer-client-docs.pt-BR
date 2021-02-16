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
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="c3396-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="c3396-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="c3396-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3396-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3396-105">Baixa um formulário para abertura.</span><span class="sxs-lookup"><span data-stu-id="c3396-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="c3396-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3396-106">Parameters</span></span>

 <span data-ttu-id="c3396-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c3396-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="c3396-108">[in] Um alça para a janela pai do indicador de progresso que é exibido enquanto o formulário é baixado.</span><span class="sxs-lookup"><span data-stu-id="c3396-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="c3396-109">O _parâmetro ulUIParam é ignorado,_ a menos que o MAPI_DIALOG padrão seja definido no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="c3396-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="c3396-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c3396-110">_ulFlags_</span></span>
  
> <span data-ttu-id="c3396-111">[in] Uma máscara de bits de sinalizadores que controla como o formulário é baixado.</span><span class="sxs-lookup"><span data-stu-id="c3396-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="c3396-112">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="c3396-112">The following flag can be set:</span></span>
    
<span data-ttu-id="c3396-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c3396-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="c3396-114">Exibe uma interface do usuário para fornecer status ou solicitar ao usuário mais informações.</span><span class="sxs-lookup"><span data-stu-id="c3396-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="c3396-115">Se esse sinalizador não estiver definido, nenhuma interface do usuário será exibida.</span><span class="sxs-lookup"><span data-stu-id="c3396-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="c3396-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="c3396-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="c3396-117">[in] Um ponteiro para um objeto de informações de formulário para o formulário a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="c3396-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c3396-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c3396-118">Return value</span></span>

<span data-ttu-id="c3396-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3396-119">S_OK</span></span> 
  
> <span data-ttu-id="c3396-120">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="c3396-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c3396-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3396-121">Remarks</span></span>

<span data-ttu-id="c3396-122">Visualizadores de formulário chamam **o método IMAPIFormMgr::P repareForm** para baixar um formulário de um contêiner de formulário para abertura.</span><span class="sxs-lookup"><span data-stu-id="c3396-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="c3396-123">A maioria dos visualizadores de formulário não precisa chamar **PrepareForm**, porque os métodos [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) e [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) chamam **PrepareForm,** se necessário.</span><span class="sxs-lookup"><span data-stu-id="c3396-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="c3396-124">Você pode usar **o PrepareForm** para obter as bibliotecas de vínculo dinâmico (DLLs) e outros arquivos associados a um formulário para modificá-los.</span><span class="sxs-lookup"><span data-stu-id="c3396-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="c3396-125">Se o formulário modificado for carregado de volta em seu contêiner de formulário, ele deverá ser reinstalado.</span><span class="sxs-lookup"><span data-stu-id="c3396-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c3396-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3396-126">See also</span></span>



[<span data-ttu-id="c3396-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="c3396-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="c3396-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="c3396-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="c3396-129">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c3396-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

