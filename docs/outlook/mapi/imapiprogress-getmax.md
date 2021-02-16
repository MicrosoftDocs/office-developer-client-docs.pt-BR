---
title: IMAPIProgressGetMax
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMax
api_type:
- COM
ms.assetid: 88a910ed-b55a-4e5b-a43d-eb3ea795a70e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 64b6235151c7700a24992bc1d4394553a53c0464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436199"
---
# <a name="imapiprogressgetmax"></a><span data-ttu-id="e1831-103">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="e1831-103">IMAPIProgress::GetMax</span></span>

  
  
<span data-ttu-id="e1831-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1831-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1831-105">Retorna o número máximo de itens na operação para o qual as informações de progresso são exibidas.</span><span class="sxs-lookup"><span data-stu-id="e1831-105">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a><span data-ttu-id="e1831-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1831-106">Parameters</span></span>

 <span data-ttu-id="e1831-107">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="e1831-107">_lpulMax_</span></span>
  
> <span data-ttu-id="e1831-108">[out] Um ponteiro para o número máximo de itens na operação.</span><span class="sxs-lookup"><span data-stu-id="e1831-108">[out] A pointer to the maximum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e1831-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e1831-109">Return value</span></span>

<span data-ttu-id="e1831-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e1831-110">S_OK</span></span> 
  
> <span data-ttu-id="e1831-111">O número máximo de itens na operação foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="e1831-111">The maximum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1831-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1831-112">Remarks</span></span>

<span data-ttu-id="e1831-113">O valor máximo representa o final da operação em formato numérico.</span><span class="sxs-lookup"><span data-stu-id="e1831-113">The maximum value represents the end of the operation in numeric form.</span></span> <span data-ttu-id="e1831-114">O valor pode ser um valor máximo global, usado para representar o escopo de toda a exibição do progresso, ou um valor local, usado para representar apenas uma parte da exibição.</span><span class="sxs-lookup"><span data-stu-id="e1831-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="e1831-115">O valor da configuração do sinalizador afeta se o objeto de progresso entende o valor máximo para ser local ou global.</span><span class="sxs-lookup"><span data-stu-id="e1831-115">The value of the flag setting affects whether the progress object understands the maximum value to be local or global.</span></span> <span data-ttu-id="e1831-116">Quando o MAPI_TOP_LEVEL é definido, o valor máximo é considerado global e é usado para calcular o progresso de toda a operação.</span><span class="sxs-lookup"><span data-stu-id="e1831-116">When the MAPI_TOP_LEVEL flag is set, the maximum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="e1831-117">Quando MAPI_TOP_LEVEL não estiver definido, o valor máximo será considerado local e os provedores o usarão internamente para exibir o progresso de subobjetos de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="e1831-117">When MAPI_TOP_LEVEL is not set, the maximum value is considered to be local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="e1831-118">Os objetos de progresso salvam o valor máximo local apenas para re devolvê-lo a um provedor por meio de uma **chamada GetMax.**</span><span class="sxs-lookup"><span data-stu-id="e1831-118">Progress objects save the local maximum value only to return it to a provider through a **GetMax** call.</span></span> 
  
<span data-ttu-id="e1831-119">Para saber mais sobre como e quando fazer chamadas para um objeto de progresso, confira o tópico [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="e1831-119">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e1831-120">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="e1831-120">Notes to implementers</span></span>

<span data-ttu-id="e1831-121">Inicialize o valor máximo para 1000.</span><span class="sxs-lookup"><span data-stu-id="e1831-121">Initialize the maximum value to 1000.</span></span> <span data-ttu-id="e1831-122">Para redefinir esse valor, os provedores de serviços podem chamar o método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md).</span><span class="sxs-lookup"><span data-stu-id="e1831-122">Service providers can reset this value by calling the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> <span data-ttu-id="e1831-123">Para obter mais informações sobre como implementar **GetMax** e outros [métodos IMAPIProgress,](imapiprogressiunknown.md) consulte [Implementando um indicador de progresso.](implementing-a-progress-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="e1831-123">For more information about how to implement **GetMax** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e1831-124">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e1831-124">MFCMAPI reference</span></span>

<span data-ttu-id="e1831-125">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e1831-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e1831-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e1831-126">**File**</span></span>|<span data-ttu-id="e1831-127">**Função**</span><span class="sxs-lookup"><span data-stu-id="e1831-127">**Function**</span></span>|<span data-ttu-id="e1831-128">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="e1831-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1831-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="e1831-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="e1831-130">CMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="e1831-130">CMAPIProgress::GetMax</span></span>  <br/> |<span data-ttu-id="e1831-131">MFCMAPI usa o **método IMAPIProgress::GetMax** para obter o valor máximo do objeto de progresso.</span><span class="sxs-lookup"><span data-stu-id="e1831-131">MFCMAPI uses the **IMAPIProgress::GetMax** method to get the maximum value for the progress object.</span></span> <span data-ttu-id="e1831-132">Retornará 1000, a menos que os limites tenham sido definidos anteriormente com o **método IMAPIProgress::SetLimits.**</span><span class="sxs-lookup"><span data-stu-id="e1831-132">Returns 1000 unless limits have previously been set with the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1831-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1831-133">See also</span></span>



[<span data-ttu-id="e1831-134">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="e1831-134">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="e1831-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="e1831-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="e1831-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="e1831-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="e1831-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1831-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="e1831-138">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e1831-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="e1831-139">Exibir um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="e1831-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="e1831-140">Como implementar um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="e1831-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

