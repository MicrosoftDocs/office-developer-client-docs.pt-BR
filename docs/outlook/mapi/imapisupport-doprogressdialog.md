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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 527a7bb3201a4a6b1bc0807136bc88b80c189de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767244"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="9d884-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="9d884-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="9d884-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d884-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d884-105">Recupera um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="9d884-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="9d884-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d884-106">Parameters</span></span>

 <span data-ttu-id="9d884-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9d884-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="9d884-108">[in] Um identificador para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="9d884-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="9d884-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9d884-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9d884-110">[in] Uma bitmask dos sinalizadores que controla como o objeto de progresso deve calcular o progresso.</span><span class="sxs-lookup"><span data-stu-id="9d884-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="9d884-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="9d884-111">The following flag can be set:</span></span>
    
<span data-ttu-id="9d884-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="9d884-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="9d884-113">Progresso é calculado para um item de nível superior, como uma pasta pai.</span><span class="sxs-lookup"><span data-stu-id="9d884-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="9d884-114">O objeto de progresso deve usar os valores nos parâmetros do método [IMAPIProgress::Progress](imapiprogress-progress.md) de _ulCount_ e _ulTotal_ — que indicam o item atual e o total de itens na operação, respectivamente — para incrementar o progresso indicador para a operação.</span><span class="sxs-lookup"><span data-stu-id="9d884-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="9d884-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="9d884-115">_lppProgress_</span></span>
  
> <span data-ttu-id="9d884-116">[out] Um ponteiro para um ponteiro para o objeto de andamento.</span><span class="sxs-lookup"><span data-stu-id="9d884-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9d884-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9d884-117">Return value</span></span>

<span data-ttu-id="9d884-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9d884-118">S_OK</span></span> 
  
> <span data-ttu-id="9d884-119">O objeto de andamento foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="9d884-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d884-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d884-120">Remarks</span></span>

<span data-ttu-id="9d884-121">O método **IMAPISupport::DoProgressDialog** é implementado para endereço livro e mensagem provedor suporte objetos store.</span><span class="sxs-lookup"><span data-stu-id="9d884-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="9d884-122">Esses provedores chamarem **DoProgressDialog** para acessar a implementação de MAPI da interface [IMAPIProgress](imapiprogressiunknown.md) , que calcula as informações de andamento e exibe uma caixa de diálogo padrão.</span><span class="sxs-lookup"><span data-stu-id="9d884-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="9d884-123">Para obter informações sobre como usar um objeto de progresso e a interface de **IMAPIProgress** , consulte [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="9d884-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9d884-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d884-124">See also</span></span>



[<span data-ttu-id="9d884-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d884-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="9d884-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="9d884-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="9d884-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d884-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="9d884-128">Exibir um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="9d884-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

