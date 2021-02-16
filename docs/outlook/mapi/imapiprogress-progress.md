---
title: IMAPIProgressProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.Progress
api_type:
- COM
ms.assetid: edbf7623-a64e-43b8-8379-e3cde2433d91
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3cf639286a504b9edb600214d13dbe50710e76a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435492"
---
# <a name="imapiprogressprogress"></a><span data-ttu-id="0d101-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="0d101-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="0d101-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d101-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d101-105">Atualiza o indicador de progresso com uma exibição do progresso conforme ele é feito na direção da conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="0d101-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="0d101-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d101-106">Parameters</span></span>

 <span data-ttu-id="0d101-107">_ulValue_</span><span class="sxs-lookup"><span data-stu-id="0d101-107">_ulValue_</span></span>
  
> <span data-ttu-id="0d101-108">[in] Um número que indica o nível atual de progresso (calculado a partir dos parâmetros  _ulCount_ e  _ulTotal_ ou dos parâmetros  _lpulMin_ e  _lpulMax_ do método [IMAPIProgress::SetLimits)](imapiprogress-setlimits.md) entre o limite inferior global e o limite superior global.</span><span class="sxs-lookup"><span data-stu-id="0d101-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="0d101-109">_ulCount_</span><span class="sxs-lookup"><span data-stu-id="0d101-109">_ulCount_</span></span>
  
> <span data-ttu-id="0d101-110">[in] Um número que indica o item processado no momento em relação ao total.</span><span class="sxs-lookup"><span data-stu-id="0d101-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="0d101-111">_ulTotal_</span><span class="sxs-lookup"><span data-stu-id="0d101-111">_ulTotal_</span></span>
  
> <span data-ttu-id="0d101-112">[in] O número total de itens a serem processados durante a operação.</span><span class="sxs-lookup"><span data-stu-id="0d101-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d101-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0d101-113">Return value</span></span>

<span data-ttu-id="0d101-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d101-114">S_OK</span></span> 
  
> <span data-ttu-id="0d101-115">O indicador de progresso foi atualizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="0d101-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="0d101-116">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="0d101-116">Notes to implementers</span></span>

<span data-ttu-id="0d101-117">O  _parâmetro ulValue_ será igual ao valor mínimo global somente no início da operação e ao valor máximo global somente na conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="0d101-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="0d101-118">Use os  _parâmetros ulCount_ e  _ulTotal,_ se disponíveis, para exibir uma mensagem opcional, como "5 itens concluídos em 10".</span><span class="sxs-lookup"><span data-stu-id="0d101-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="0d101-119">Se  _ulCount_ e  _ulTotal_ são definidos como 0, decida se deve alterar visualmente o indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="0d101-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="0d101-120">Alguns provedores de serviços configuram esses parâmetros como 0 para indicar que estão processando um subobjeto cujo progresso é monitorado em relação a um objeto pai.</span><span class="sxs-lookup"><span data-stu-id="0d101-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="0d101-121">Nessa situação, faz sentido alterar a exibição somente quando o objeto pai relata progresso.</span><span class="sxs-lookup"><span data-stu-id="0d101-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="0d101-122">Alguns provedores de serviços passam 0 para esses parâmetros sempre.</span><span class="sxs-lookup"><span data-stu-id="0d101-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="0d101-123">Para obter mais informações sobre como implementar **o progresso** e os outros [métodos IMAPIProgress,](imapiprogressiunknown.md) consulte [Implementando um indicador de progresso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="0d101-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="0d101-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="0d101-124">Notes to callers</span></span>

<span data-ttu-id="0d101-125">Nem todos os três parâmetros para **IMAPIProgress::P ess** são necessários.</span><span class="sxs-lookup"><span data-stu-id="0d101-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="0d101-126">O único parâmetro necessário é  _ulValue_, um número que indica a porcentagem de progresso.</span><span class="sxs-lookup"><span data-stu-id="0d101-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="0d101-127">Se o MAPI_TOP_LEVEL sinalizador estiver definido, você também poderá passar uma contagem de objetos e um total de objetos.</span><span class="sxs-lookup"><span data-stu-id="0d101-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="0d101-128">Algumas implementações usam esses valores para exibir uma frase como "5 itens concluídos em 10" com o indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="0d101-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="0d101-129">Se você estiver copiando todas as mensagens em uma única pasta, de definir  _ulTotal_ como o número total de mensagens sendo copiadas.</span><span class="sxs-lookup"><span data-stu-id="0d101-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="0d101-130">Se você estiver copiando uma pasta, de definir  _ulTotal_ como o número de subpastas na pasta.</span><span class="sxs-lookup"><span data-stu-id="0d101-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="0d101-131">Se a pasta a ser copiada não contiver subpastas e apenas mensagens, de definida  _como_ 1.</span><span class="sxs-lookup"><span data-stu-id="0d101-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="0d101-132">Para saber mais sobre como e quando fazer chamadas para um objeto de progresso, confira o tópico [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="0d101-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0d101-133">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0d101-133">MFCMAPI reference</span></span>

<span data-ttu-id="0d101-134">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d101-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0d101-135">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="0d101-135">**File**</span></span>|<span data-ttu-id="0d101-136">**Função**</span><span class="sxs-lookup"><span data-stu-id="0d101-136">**Function**</span></span>|<span data-ttu-id="0d101-137">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="0d101-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0d101-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="0d101-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="0d101-139">CMAPIProgress::P ress</span><span class="sxs-lookup"><span data-stu-id="0d101-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="0d101-140">MFCMAPI usa o método **IMAPIProgress::P ess** para atualizar a barra de status MFCMAPI com a porcentagem atual de progresso, calculada a partir de  _uValue_ e os valores máximo e mínimo atuais.</span><span class="sxs-lookup"><span data-stu-id="0d101-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d101-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d101-141">See also</span></span>



[<span data-ttu-id="0d101-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="0d101-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="0d101-143">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d101-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="0d101-144">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="0d101-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="0d101-145">Exibir um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="0d101-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="0d101-146">Como implementar um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="0d101-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

