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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285203"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="f473f-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="f473f-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="f473f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f473f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f473f-105">Recupera um objeto Progress que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="f473f-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="f473f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f473f-106">Parameters</span></span>

 <span data-ttu-id="f473f-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f473f-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="f473f-108">no Uma alça para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="f473f-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="f473f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f473f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f473f-110">no Uma bitmask de sinalizadores que controla como o objeto Progress deve calcular o andamento.</span><span class="sxs-lookup"><span data-stu-id="f473f-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="f473f-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="f473f-111">The following flag can be set:</span></span>
    
<span data-ttu-id="f473f-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="f473f-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="f473f-113">O andamento é calculado para um item de nível superior, como uma pasta pai.</span><span class="sxs-lookup"><span data-stu-id="f473f-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="f473f-114">O objeto Progress deve usar os valores no [método imapiprogress::P rogress](imapiprogress-progress.md) do método _ulCount_ e _ulTotal_ parâmetros, que indicam o item atual e o total de itens na operação, respectivamente, para incrementar o progresso indicador para a operação.</span><span class="sxs-lookup"><span data-stu-id="f473f-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="f473f-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="f473f-115">_lppProgress_</span></span>
  
> <span data-ttu-id="f473f-116">bota Um ponteiro para um ponteiro para o objeto Progress.</span><span class="sxs-lookup"><span data-stu-id="f473f-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f473f-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f473f-117">Return value</span></span>

<span data-ttu-id="f473f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f473f-118">S_OK</span></span> 
  
> <span data-ttu-id="f473f-119">O objeto Progress foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="f473f-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f473f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f473f-120">Remarks</span></span>

<span data-ttu-id="f473f-121">O método **IMAPISupport::D oprogressdialog** é implementado para os objetos de suporte para o catálogo de endereços e o provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f473f-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="f473f-122">Esses provedores chamam o **DoProgressDialog** para acessar a implementação de MAPI da interface [método imapiprogress](imapiprogressiunknown.md) , que calcula as informações de progresso e exibe uma caixa de diálogo padrão.</span><span class="sxs-lookup"><span data-stu-id="f473f-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="f473f-123">Para obter informações sobre como usar um objeto Progress e a interface **método imapiprogress** , consulte [exibir um indicador de progresso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="f473f-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f473f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f473f-124">See also</span></span>



[<span data-ttu-id="f473f-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f473f-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="f473f-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="f473f-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="f473f-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f473f-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="f473f-128">Exibir um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="f473f-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

