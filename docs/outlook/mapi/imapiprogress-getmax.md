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
ms.openlocfilehash: bbd52116a108be12df7697f45df41b03adeba68e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767125"
---
# <a name="imapiprogressgetmax"></a><span data-ttu-id="fd360-103">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="fd360-103">IMAPIProgress::GetMax</span></span>

  
  
<span data-ttu-id="fd360-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd360-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd360-105">Retorna o número máximo de itens na operação para o qual andamento informações são exibidas.</span><span class="sxs-lookup"><span data-stu-id="fd360-105">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a><span data-ttu-id="fd360-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd360-106">Parameters</span></span>

 <span data-ttu-id="fd360-107">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="fd360-107">_lpulMax_</span></span>
  
> <span data-ttu-id="fd360-108">[out] Um ponteiro para o número máximo de itens na operação.</span><span class="sxs-lookup"><span data-stu-id="fd360-108">[out] A pointer to the maximum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fd360-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fd360-109">Return value</span></span>

<span data-ttu-id="fd360-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd360-110">S_OK</span></span> 
  
> <span data-ttu-id="fd360-111">O número máximo de itens na operação terem sido recuperado.</span><span class="sxs-lookup"><span data-stu-id="fd360-111">The maximum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd360-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd360-112">Remarks</span></span>

<span data-ttu-id="fd360-113">O valor máximo representa o fim da operação no formulário numérico.</span><span class="sxs-lookup"><span data-stu-id="fd360-113">The maximum value represents the end of the operation in numeric form.</span></span> <span data-ttu-id="fd360-114">O valor pode ser um valor máximo global, usado para representar o escopo da tela inteira progresso, ou um valor local, usado para representar a apenas uma parte da tela.</span><span class="sxs-lookup"><span data-stu-id="fd360-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="fd360-115">O valor da configuração de sinalizador afeta se o objeto de progresso entende o valor máximo seja local ou global.</span><span class="sxs-lookup"><span data-stu-id="fd360-115">The value of the flag setting affects whether the progress object understands the maximum value to be local or global.</span></span> <span data-ttu-id="fd360-116">Quando o sinalizador MAPI_TOP_LEVEL estiver definido, o valor máximo é considerado como global e é usado para calcular o progresso de toda a operação.</span><span class="sxs-lookup"><span data-stu-id="fd360-116">When the MAPI_TOP_LEVEL flag is set, the maximum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="fd360-117">Quando MAPI_TOP_LEVEL não estiver definida, o valor máximo é considerado como local e provedores usam internamente para exibir o progresso subobjetos de nível inferiores.</span><span class="sxs-lookup"><span data-stu-id="fd360-117">When MAPI_TOP_LEVEL is not set, the maximum value is considered to be local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="fd360-118">Objetos de progresso salvar o valor máximo local somente para retorná-lo a um provedor através de uma chamada **GetMax** .</span><span class="sxs-lookup"><span data-stu-id="fd360-118">Progress objects save the local maximum value only to return it to a provider through a **GetMax** call.</span></span> 
  
<span data-ttu-id="fd360-119">Para obter mais informações sobre como e quando fazer chamadas para um objeto de progresso, consulte [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="fd360-119">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fd360-120">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="fd360-120">Notes to implementers</span></span>

<span data-ttu-id="fd360-121">Inicialize o valor máximo a 1000.</span><span class="sxs-lookup"><span data-stu-id="fd360-121">Initialize the maximum value to 1000.</span></span> <span data-ttu-id="fd360-122">Provedores de serviços podem redefinir esse valor chamando o método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) .</span><span class="sxs-lookup"><span data-stu-id="fd360-122">Service providers can reset this value by calling the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> <span data-ttu-id="fd360-123">Para obter mais informações sobre como implementar **GetMax** e outros métodos [IMAPIProgress](imapiprogressiunknown.md) , consulte [Implementando um indicador de progresso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="fd360-123">For more information about how to implement **GetMax** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fd360-124">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fd360-124">MFCMAPI reference</span></span>

<span data-ttu-id="fd360-125">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fd360-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fd360-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="fd360-126">**File**</span></span>|<span data-ttu-id="fd360-127">**Function**</span><span class="sxs-lookup"><span data-stu-id="fd360-127">**Function**</span></span>|<span data-ttu-id="fd360-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="fd360-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fd360-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="fd360-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="fd360-130">CMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="fd360-130">CMAPIProgress::GetMax</span></span>  <br/> |<span data-ttu-id="fd360-131">MFCMAPI usa o método **IMAPIProgress::GetMax** para obter o valor máximo para o objeto de andamento.</span><span class="sxs-lookup"><span data-stu-id="fd360-131">MFCMAPI uses the **IMAPIProgress::GetMax** method to get the maximum value for the progress object.</span></span> <span data-ttu-id="fd360-132">Retorna a 1000, a menos que limites anteriormente foram definidos com o método **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="fd360-132">Returns 1000 unless limits have previously been set with the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd360-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd360-133">See also</span></span>



[<span data-ttu-id="fd360-134">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="fd360-134">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="fd360-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="fd360-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="fd360-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="fd360-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="fd360-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fd360-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="fd360-138">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="fd360-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="fd360-139">Exibir um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="fd360-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="fd360-140">Implementar um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="fd360-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

