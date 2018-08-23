---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 010f69b70324d4280a34d2fe06d670e07d922d86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586771"
---
# <a name="imapiprogresssetlimits"></a><span data-ttu-id="d05b3-103">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="d05b3-103">IMAPIProgress::SetLimits</span></span>

  
  
<span data-ttu-id="d05b3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d05b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d05b3-105">Define os limites inferiores e superiores para o número de itens da operação e os sinalizadores que controlam como as informações sobre o andamento é calculada para a operação.</span><span class="sxs-lookup"><span data-stu-id="d05b3-105">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d05b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d05b3-106">Parameters</span></span>

 <span data-ttu-id="d05b3-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="d05b3-107">_lpulMin_</span></span>
  
> <span data-ttu-id="d05b3-108">[in] Um ponteiro para uma variável que contenha o limite inferior dos itens na operação.</span><span class="sxs-lookup"><span data-stu-id="d05b3-108">[in] A pointer to a variable that contains the lower limit of items in the operation.</span></span>
    
 <span data-ttu-id="d05b3-109">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="d05b3-109">_lpulMax_</span></span>
  
> <span data-ttu-id="d05b3-110">[in] Um ponteiro para uma variável que contenha o limite superior dos itens na operação.</span><span class="sxs-lookup"><span data-stu-id="d05b3-110">[in] A pointer to a variable that contains the upper limit of items in the operation.</span></span>
    
 <span data-ttu-id="d05b3-111">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="d05b3-111">_lpulFlags_</span></span>
  
> <span data-ttu-id="d05b3-112">[in] Uma bitmask dos sinalizadores que controla o nível de operação em andamento da qual as informações são calculadas.</span><span class="sxs-lookup"><span data-stu-id="d05b3-112">[in] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="d05b3-113">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="d05b3-113">The following flag can be set:</span></span>
    
<span data-ttu-id="d05b3-114">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="d05b3-114">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="d05b3-115">Usa os valores do método [IMAPIProgress::Progress](imapiprogress-progress.md) _ulCount_ _ulTotal_ parâmetros e, que indica o item atualmente processado e o total de itens, respectivamente, para o progresso de incremento sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="d05b3-115">Uses the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters, which indicate the currently processed item and the total items, respectively, to increment progress on the operation.</span></span> <span data-ttu-id="d05b3-116">Quando esse sinalizador estiver definido, os valores dos limites inferiores e superiores globais têm a ser definido.</span><span class="sxs-lookup"><span data-stu-id="d05b3-116">When this flag is set, the values of the global lower and upper limits have to be set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d05b3-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d05b3-117">Return value</span></span>

<span data-ttu-id="d05b3-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d05b3-118">S_OK</span></span> 
  
> <span data-ttu-id="d05b3-119">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="d05b3-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d05b3-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="d05b3-120">Remarks</span></span>

<span data-ttu-id="d05b3-121">Provedores de serviços de chamarem o método de **IMAPIProgress::SetLimits** para definir ou limpar o sinalizador MAPI_TOP_LEVEL e para definir os valores máximo e mínimo de globais e locais.</span><span class="sxs-lookup"><span data-stu-id="d05b3-121">Service providers call the **IMAPIProgress::SetLimits** method to set or clear the MAPI_TOP_LEVEL flag and to set local and global minimum and maximum values.</span></span> <span data-ttu-id="d05b3-122">O valor da configuração de sinalizador afeta se o objeto de progresso entende os valores mínimos e máximo para ser local ou global.</span><span class="sxs-lookup"><span data-stu-id="d05b3-122">The value of the flag setting affects whether the progress object understands the minimum and maximum values to be local or global.</span></span> <span data-ttu-id="d05b3-123">Quando o sinalizador MAPI_TOP_LEVEL estiver definido, esses valores são considerados globais e são usados para calcular o progresso de toda a operação.</span><span class="sxs-lookup"><span data-stu-id="d05b3-123">When the MAPI_TOP_LEVEL flag is set, these values are considered global and are used to calculate progress for the entire operation.</span></span> <span data-ttu-id="d05b3-124">Objetos de progresso inicializar o valor mínimo global como 1 e o valor máximo global a 1000.</span><span class="sxs-lookup"><span data-stu-id="d05b3-124">Progress objects initialize the global minimum value to 1 and the global maximum value to 1000.</span></span> 
  
<span data-ttu-id="d05b3-125">Quando MAPI_TOP_LEVEL não estiver definida, os valores mínimos e máximo são considerados locais e provedores de usá-los internamente para exibir o progresso de subobjetos de nível inferiores.</span><span class="sxs-lookup"><span data-stu-id="d05b3-125">When MAPI_TOP_LEVEL is not set, the minimum and maximum values are considered local, and providers use them internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="d05b3-126">Objetos de progresso salvar os valores mínimos e máximo locais somente para que pode ser retornados para provedores quando os métodos [IMAPIProgress::GetMin](imapiprogress-getmin.md) e [IMAPIProgress::GetMax](imapiprogress-getmax.md) são chamados.</span><span class="sxs-lookup"><span data-stu-id="d05b3-126">Progress objects save the local minimum and maximum values only so that they can be returned to providers when the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods are called.</span></span> 
  
<span data-ttu-id="d05b3-127">Para obter mais informações sobre como implementar **SetLimits** e outros métodos [IMAPIProgress](imapiprogressiunknown.md) , consulte [Implementando um indicador de progresso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="d05b3-127">For more information about how to implement **SetLimits** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="d05b3-128">Para obter mais informações sobre como e quando fazer chamadas para um objeto de progresso, consulte [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="d05b3-128">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d05b3-129">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d05b3-129">MFCMAPI reference</span></span>

<span data-ttu-id="d05b3-130">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d05b3-130">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d05b3-131">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d05b3-131">**File**</span></span>|<span data-ttu-id="d05b3-132">**Function**</span><span class="sxs-lookup"><span data-stu-id="d05b3-132">**Function**</span></span>|<span data-ttu-id="d05b3-133">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d05b3-133">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d05b3-134">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="d05b3-134">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="d05b3-135">CMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="d05b3-135">CMAPIProgress::SetLimits</span></span>  <br/> |<span data-ttu-id="d05b3-136">MFCMAPI usa o método **IMAPIProgress::SetLimits** para definir os sinalizadores para o objeto de progresso e limites máximo e mínimos.</span><span class="sxs-lookup"><span data-stu-id="d05b3-136">MFCMAPI uses the **IMAPIProgress::SetLimits** method to set the maximum and minimum limits and flags for the progress object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d05b3-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="d05b3-137">See also</span></span>



[<span data-ttu-id="d05b3-138">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="d05b3-138">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="d05b3-139">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="d05b3-139">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="d05b3-140">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="d05b3-140">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="d05b3-141">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d05b3-141">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="d05b3-142">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d05b3-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d05b3-143">Exibir um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="d05b3-143">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="d05b3-144">Implementar um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="d05b3-144">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

