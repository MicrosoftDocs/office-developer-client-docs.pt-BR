---
title: IMAPIProgressGetMin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMin
api_type:
- COM
ms.assetid: caceddf1-0f7c-47b5-97bf-17ffe3440a6c
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: ab92aee6a8254a16c48352e371b711932bbe7427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767128"
---
# <a name="imapiprogressgetmin"></a><span data-ttu-id="58848-103">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="58848-103">IMAPIProgress::GetMin</span></span>

  
  
<span data-ttu-id="58848-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58848-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58848-105">Retorna o valor mínimo no método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) para qual andamento informações são exibidas.</span><span class="sxs-lookup"><span data-stu-id="58848-105">Returns the minimum value in the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span> 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a><span data-ttu-id="58848-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="58848-106">Parameters</span></span>

 <span data-ttu-id="58848-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="58848-107">_lpulMin_</span></span>
  
> <span data-ttu-id="58848-108">[out] Um ponteiro para o número mínimo de itens na operação.</span><span class="sxs-lookup"><span data-stu-id="58848-108">[out] A pointer to the minimum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="58848-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="58848-109">Return value</span></span>

<span data-ttu-id="58848-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="58848-110">S_OK</span></span> 
  
> <span data-ttu-id="58848-111">O número mínimo de itens na operação terem sido recuperado.</span><span class="sxs-lookup"><span data-stu-id="58848-111">The minimum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58848-112">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="58848-112">Remarks</span></span>

<span data-ttu-id="58848-113">O valor mínimo representa o início da operação no formulário numérico.</span><span class="sxs-lookup"><span data-stu-id="58848-113">The minimum value represents the start of the operation in numeric form.</span></span> <span data-ttu-id="58848-114">O valor pode ser um valor máximo global, usado para representar o escopo da tela inteira progresso, ou um valor local, usado para representar a apenas uma parte da tela.</span><span class="sxs-lookup"><span data-stu-id="58848-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="58848-115">O valor da configuração de sinalizador afeta se o objeto de progresso entende o valor mínimo seja local ou global.</span><span class="sxs-lookup"><span data-stu-id="58848-115">The value of the flag setting affects whether the progress object understands the minimum value to be local or global.</span></span> <span data-ttu-id="58848-116">Quando o sinalizador MAPI_TOP_LEVEL estiver definido, o valor mínimo é considerado como global e é usado para calcular o progresso de toda a operação.</span><span class="sxs-lookup"><span data-stu-id="58848-116">When the MAPI_TOP_LEVEL flag is set, the minimum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="58848-117">Quando MAPI_TOP_LEVEL não estiver definida, o valor mínimo é considerado local e provedores usam internamente para exibir o progresso subobjetos de nível inferiores.</span><span class="sxs-lookup"><span data-stu-id="58848-117">When MAPI_TOP_LEVEL is not set, the minimum value is considered local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="58848-118">Objetos de progresso salvar o valor mínimo local somente para retorná-lo a um provedor através de uma chamada **GetMin** .</span><span class="sxs-lookup"><span data-stu-id="58848-118">Progress objects save the local minimum value only to return it to a provider through a **GetMin** call.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="58848-119">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="58848-119">Notes to implementers</span></span>

<span data-ttu-id="58848-120">Inicialize o valor mínimo como 1.</span><span class="sxs-lookup"><span data-stu-id="58848-120">Initialize the minimum value to 1.</span></span> <span data-ttu-id="58848-121">Provedores de serviços podem redefinir esse valor chamando o método **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="58848-121">Service providers can reset this value by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="58848-122">Para obter mais informações sobre como implementar **GetMin** e outros métodos [IMAPIProgress](imapiprogressiunknown.md) , consulte [Implementando um indicador de progresso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="58848-122">For more information about how to implement **GetMin** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="58848-123">Para obter mais informações sobre como e quando fazer chamadas para um objeto de progresso, consulte [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="58848-123">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="58848-124">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="58848-124">MFCMAPI reference</span></span>

<span data-ttu-id="58848-125">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="58848-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="58848-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="58848-126">**File**</span></span>|<span data-ttu-id="58848-127">**Function**</span><span class="sxs-lookup"><span data-stu-id="58848-127">**Function**</span></span>|<span data-ttu-id="58848-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="58848-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="58848-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="58848-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="58848-130">CMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="58848-130">CMAPIProgress::GetMin</span></span>  <br/> |<span data-ttu-id="58848-131">MFCMAPI usa o método **IMAPIProgress::GetMin** para obter o valor mínimo para o indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="58848-131">MFCMAPI uses the **IMAPIProgress::GetMin** method to get the minimum value for the progress indicator.</span></span> <span data-ttu-id="58848-132">Retornará 1, a menos que limites tenham sido definidos anteriormente chamando o método **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="58848-132">Returns 1 unless limits have been previously set by calling the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58848-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="58848-133">See also</span></span>



[<span data-ttu-id="58848-134">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="58848-134">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="58848-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="58848-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="58848-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="58848-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="58848-137">IMAPIProgress: IUnknown</span><span class="sxs-lookup"><span data-stu-id="58848-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="58848-138">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="58848-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="58848-139">Exibir um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="58848-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="58848-140">Implementando um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="58848-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

