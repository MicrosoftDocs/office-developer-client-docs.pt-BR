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
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421463"
---
# <a name="imapiprogresssetlimits"></a><span data-ttu-id="1d564-103">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="1d564-103">IMAPIProgress::SetLimits</span></span>

  
  
<span data-ttu-id="1d564-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d564-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d564-105">Define os limites inferior e superior para o número de itens na operação e os sinalizadores que controlam como as informações de progresso são calculadas para a operação.</span><span class="sxs-lookup"><span data-stu-id="1d564-105">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1d564-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d564-106">Parameters</span></span>

 <span data-ttu-id="1d564-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="1d564-107">_lpulMin_</span></span>
  
> <span data-ttu-id="1d564-108">no Um ponteiro para uma variável que contém o limite inferior dos itens na operação.</span><span class="sxs-lookup"><span data-stu-id="1d564-108">[in] A pointer to a variable that contains the lower limit of items in the operation.</span></span>
    
 <span data-ttu-id="1d564-109">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="1d564-109">_lpulMax_</span></span>
  
> <span data-ttu-id="1d564-110">no Um ponteiro para uma variável que contém o limite superior de itens na operação.</span><span class="sxs-lookup"><span data-stu-id="1d564-110">[in] A pointer to a variable that contains the upper limit of items in the operation.</span></span>
    
 <span data-ttu-id="1d564-111">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="1d564-111">_lpulFlags_</span></span>
  
> <span data-ttu-id="1d564-112">no Uma bitmask de sinalizadores que controla o nível de operação no qual as informações de progresso são calculadas.</span><span class="sxs-lookup"><span data-stu-id="1d564-112">[in] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="1d564-113">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="1d564-113">The following flag can be set:</span></span>
    
<span data-ttu-id="1d564-114">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="1d564-114">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="1d564-115">Usa os valores dos parâmetros _ulCount_ e _UlTotal_ do método [método imapiprogress::P rogress](imapiprogress-progress.md) , que indicam o item processado atualmente e o total de itens, respectivamente, para incrementar o progresso na operação.</span><span class="sxs-lookup"><span data-stu-id="1d564-115">Uses the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters, which indicate the currently processed item and the total items, respectively, to increment progress on the operation.</span></span> <span data-ttu-id="1d564-116">Quando esse sinalizador é definido, os valores dos limites global inferior e superior precisam ser definidos.</span><span class="sxs-lookup"><span data-stu-id="1d564-116">When this flag is set, the values of the global lower and upper limits have to be set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1d564-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1d564-117">Return value</span></span>

<span data-ttu-id="1d564-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d564-118">S_OK</span></span> 
  
> <span data-ttu-id="1d564-119">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="1d564-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d564-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d564-120">Remarks</span></span>

<span data-ttu-id="1d564-121">Os provedores de serviços chamam o método **método imapiprogress::** setlimits para definir ou limpar o sinalizador MAPI_TOP_LEVEL e para definir os valores mínimos e globais locais e máximos.</span><span class="sxs-lookup"><span data-stu-id="1d564-121">Service providers call the **IMAPIProgress::SetLimits** method to set or clear the MAPI_TOP_LEVEL flag and to set local and global minimum and maximum values.</span></span> <span data-ttu-id="1d564-122">O valor da configuração do sinalizador afeta se o objeto Progress entende os valores mínimo e máximo para serem local ou global.</span><span class="sxs-lookup"><span data-stu-id="1d564-122">The value of the flag setting affects whether the progress object understands the minimum and maximum values to be local or global.</span></span> <span data-ttu-id="1d564-123">Quando o sinalizador MAPI_TOP_LEVEL é definido, esses valores são considerados globais e são usados para calcular o progresso de toda a operação.</span><span class="sxs-lookup"><span data-stu-id="1d564-123">When the MAPI_TOP_LEVEL flag is set, these values are considered global and are used to calculate progress for the entire operation.</span></span> <span data-ttu-id="1d564-124">Os objetos Progress inicializam o valor mínimo global como 1 e o valor global máximo como 1000.</span><span class="sxs-lookup"><span data-stu-id="1d564-124">Progress objects initialize the global minimum value to 1 and the global maximum value to 1000.</span></span> 
  
<span data-ttu-id="1d564-125">Quando MAPI_TOP_LEVEL não estiver definido, os valores mínimo e máximo serão considerados locais e os provedores os usarão internamente para exibir o progresso dos subobjetos de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="1d564-125">When MAPI_TOP_LEVEL is not set, the minimum and maximum values are considered local, and providers use them internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="1d564-126">Os objetos Progress salvam os valores mínimo e máximo locais apenas para que eles possam ser retornados aos provedores quando os métodos [método imapiprogress:: GetMin](imapiprogress-getmin.md) e [método imapiprogress:: GetMax](imapiprogress-getmax.md) são chamados.</span><span class="sxs-lookup"><span data-stu-id="1d564-126">Progress objects save the local minimum and maximum values only so that they can be returned to providers when the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods are called.</span></span> 
  
<span data-ttu-id="1d564-127">Para obter mais informações sobre como implementar \*\*\*\* setlimits e os outros métodos do [método imapiprogress](imapiprogressiunknown.md) , consulte [implementando um indicador de progresso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="1d564-127">For more information about how to implement **SetLimits** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="1d564-128">Para saber mais sobre como e quando fazer chamadas para um objeto de progresso, confira o tópico [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="1d564-128">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1d564-129">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1d564-129">MFCMAPI reference</span></span>

<span data-ttu-id="1d564-130">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1d564-130">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1d564-131">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1d564-131">**File**</span></span>|<span data-ttu-id="1d564-132">**Função**</span><span class="sxs-lookup"><span data-stu-id="1d564-132">**Function**</span></span>|<span data-ttu-id="1d564-133">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="1d564-133">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1d564-134">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="1d564-134">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="1d564-135">CMAPIProgress:: setLimits</span><span class="sxs-lookup"><span data-stu-id="1d564-135">CMAPIProgress::SetLimits</span></span>  <br/> |<span data-ttu-id="1d564-136">MFCMAPI usa o método **método imapiprogress::** setlimits para definir os limites máximo e mínimo e os sinalizadores para o objeto Progress.</span><span class="sxs-lookup"><span data-stu-id="1d564-136">MFCMAPI uses the **IMAPIProgress::SetLimits** method to set the maximum and minimum limits and flags for the progress object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d564-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d564-137">See also</span></span>



[<span data-ttu-id="1d564-138">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="1d564-138">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="1d564-139">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="1d564-139">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="1d564-140">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="1d564-140">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="1d564-141">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1d564-141">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="1d564-142">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1d564-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="1d564-143">Exibir um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="1d564-143">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="1d564-144">Como implementar um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="1d564-144">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

