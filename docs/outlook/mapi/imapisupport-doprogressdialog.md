---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3de29e9af5caa82d2e57c8fcbbdab7d5ddb19dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432580"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="90a43-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="90a43-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="90a43-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90a43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90a43-105">Recupera um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="90a43-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="90a43-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90a43-106">Parameters</span></span>

 <span data-ttu-id="90a43-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="90a43-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="90a43-108">[in] Um alça para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="90a43-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="90a43-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="90a43-109">_ulFlags_</span></span>
  
> <span data-ttu-id="90a43-110">[in] Uma bitmask de sinalizadores que controla como o objeto de progresso deve calcular o progresso.</span><span class="sxs-lookup"><span data-stu-id="90a43-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="90a43-111">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="90a43-111">The following flag can be set:</span></span>
    
<span data-ttu-id="90a43-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="90a43-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="90a43-113">O andamento é calculado para um item de nível superior, como uma pasta pai.</span><span class="sxs-lookup"><span data-stu-id="90a43-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="90a43-114">O objeto de progresso deve usar os valores nos parâmetros _ulCount_ e _ulTotal_ do método [IMAPIProgress::P ess](imapiprogress-progress.md) — que indicam o item atual e o total de itens na operação, respectivamente — para incrementar o indicador de progresso da operação.</span><span class="sxs-lookup"><span data-stu-id="90a43-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="90a43-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="90a43-115">_lppProgress_</span></span>
  
> <span data-ttu-id="90a43-116">[out] Um ponteiro para um ponteiro para o objeto de progresso.</span><span class="sxs-lookup"><span data-stu-id="90a43-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="90a43-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="90a43-117">Return value</span></span>

<span data-ttu-id="90a43-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="90a43-118">S_OK</span></span> 
  
> <span data-ttu-id="90a43-119">O objeto de progresso foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="90a43-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90a43-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="90a43-120">Remarks</span></span>

<span data-ttu-id="90a43-121">O **método IMAPISupport::D oProgressDialog** é implementado para objetos de suporte de provedor de armazenamento de endereços e de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="90a43-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="90a43-122">Esses provedores chamam **DoProgressDialog** para acessar a implementação de MAPI da interface [IMAPIProgress,](imapiprogressiunknown.md) que calcula as informações de progresso e exibe uma caixa de diálogo padrão.</span><span class="sxs-lookup"><span data-stu-id="90a43-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="90a43-123">Para obter informações sobre como usar um objeto de progresso e a interface **IMAPIProgress,** consulte [Exibir um indicador de progresso.](how-to-display-a-progress-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="90a43-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="90a43-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="90a43-124">See also</span></span>



[<span data-ttu-id="90a43-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="90a43-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="90a43-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="90a43-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="90a43-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="90a43-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="90a43-128">Exibir um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="90a43-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

