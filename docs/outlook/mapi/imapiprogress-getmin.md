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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6cd31f8ac713c21053db7ef461220a360ebeec74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404845"
---
# <a name="imapiprogressgetmin"></a><span data-ttu-id="ab0e4-103">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="ab0e4-103">IMAPIProgress::GetMin</span></span>

  
  
<span data-ttu-id="ab0e4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab0e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab0e4-105">Retorna o valor mínimo no método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) cujas informações do progresso são exibidas.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-105">Returns the minimum value in the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span> 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a><span data-ttu-id="ab0e4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab0e4-106">Parameters</span></span>

 <span data-ttu-id="ab0e4-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="ab0e4-107">_lpulMin_</span></span>
  
> <span data-ttu-id="ab0e4-108">[out] Um ponteiro para o número mínimo de itens na operação.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-108">[out] A pointer to the minimum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ab0e4-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ab0e4-109">Return value</span></span>

<span data-ttu-id="ab0e4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab0e4-110">S_OK</span></span> 
  
> <span data-ttu-id="ab0e4-111">O número mínimo de itens na operação foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-111">The minimum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab0e4-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab0e4-112">Remarks</span></span>

<span data-ttu-id="ab0e4-113">O valor mínimo representa o início da operação em formato numérico.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-113">The minimum value represents the start of the operation in numeric form.</span></span> <span data-ttu-id="ab0e4-114">O valor pode ser um valor máximo global, usado para representar o escopo de toda a exibição do progresso, ou um valor local, usado para representar apenas uma parte da exibição.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="ab0e4-115">O valor da configuração do sinalizador afeta se o objeto de progresso entende o valor mínimo como local ou global.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-115">The value of the flag setting affects whether the progress object understands the minimum value to be local or global.</span></span> <span data-ttu-id="ab0e4-116">Quando o sinalizador MAPI_TOP_LEVEL estiver definido, o valor mínimo será considerado como global e usado para calcular o progresso de toda a operação.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-116">When the MAPI_TOP_LEVEL flag is set, the minimum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="ab0e4-117">Quando MAPI_TOP_LEVEL não estiver definido, o valor mínimo será considerado como local, e os provedores o usam internamente para exibir o progresso de subobjetos de níveis inferiores.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-117">When MAPI_TOP_LEVEL is not set, the minimum value is considered local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="ab0e4-118">Os objetos de progresso salvam o valor mínimo local apenas para retorná-lo a um provedor por meio de uma chamada **GetMin**.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-118">Progress objects save the local minimum value only to return it to a provider through a **GetMin** call.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ab0e4-119">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="ab0e4-119">Notes to implementers</span></span>

<span data-ttu-id="ab0e4-120">Inicialize o valor mínimo como 1.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-120">Initialize the minimum value to 1.</span></span> <span data-ttu-id="ab0e4-121">Para redefinir esse valor, os provedores de serviços podem chamar o método **IMAPIProgress::SetLimits**.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-121">Service providers can reset this value by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="ab0e4-122">Para saber mais sobre como implementar **GetMin** e os outros métodos [IMAPIProgress](imapiprogressiunknown.md), confira [Como implementar um indicador de progresso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="ab0e4-122">For more information about how to implement **GetMin** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="ab0e4-123">Para saber mais sobre como e quando fazer chamadas para um objeto de progresso, confira o tópico [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="ab0e4-123">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ab0e4-124">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ab0e4-124">MFCMAPI reference</span></span>

<span data-ttu-id="ab0e4-125">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ab0e4-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ab0e4-126">**File**</span></span>|<span data-ttu-id="ab0e4-127">**Função**</span><span class="sxs-lookup"><span data-stu-id="ab0e4-127">**Function**</span></span>|<span data-ttu-id="ab0e4-128">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ab0e4-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ab0e4-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="ab0e4-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="ab0e4-130">CMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="ab0e4-130">CMAPIProgress::GetMin</span></span>  <br/> |<span data-ttu-id="ab0e4-131">O MFCMAPI usa o método **IMAPIProgress::GetMin** para obter o valor mínimo do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-131">MFCMAPI uses the **IMAPIProgress::GetMin** method to get the minimum value for the progress indicator.</span></span> <span data-ttu-id="ab0e4-132">Retorna 1, a menos que os limites tenham sido definidos anteriormente chamando o método **IMAPIProgress::SetLimits**.</span><span class="sxs-lookup"><span data-stu-id="ab0e4-132">Returns 1 unless limits have been previously set by calling the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab0e4-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab0e4-133">See also</span></span>



[<span data-ttu-id="ab0e4-134">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="ab0e4-134">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="ab0e4-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="ab0e4-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="ab0e4-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="ab0e4-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="ab0e4-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ab0e4-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="ab0e4-138">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ab0e4-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="ab0e4-139">Exibir um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="ab0e4-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="ab0e4-140">Como implementar um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="ab0e4-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

