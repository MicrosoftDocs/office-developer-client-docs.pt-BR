---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416437"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="8829c-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="8829c-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="8829c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8829c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8829c-105">Processa componentes individuais de uma mensagem de cada vez em um fluxo TNEF (Transport-neutral Encapsulation Format).</span><span class="sxs-lookup"><span data-stu-id="8829c-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="8829c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8829c-106">Parameters</span></span>

 <span data-ttu-id="8829c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8829c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8829c-108">no Uma bitmask de sinalizadores que controla qual componente será concluído.</span><span class="sxs-lookup"><span data-stu-id="8829c-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="8829c-109">Um ou outro dos seguintes sinalizadores devem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="8829c-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="8829c-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="8829c-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="8829c-111">O processamento será concluído para um objeto Attachment; o parâmetro _ulComponentID_ contém a propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo.</span><span class="sxs-lookup"><span data-stu-id="8829c-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="8829c-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="8829c-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="8829c-113">O processamento será concluído para um objeto Message.</span><span class="sxs-lookup"><span data-stu-id="8829c-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="8829c-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="8829c-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="8829c-115">[in] 0 para indicar o processamento de uma mensagem ou a propriedade **PR_ATTACH_NUM** de um anexo a ser processada.</span><span class="sxs-lookup"><span data-stu-id="8829c-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="8829c-116">Se o sinalizador TNEF_COMPONENT_MESSAGE estiver definido no parâmetro _parâmetroulflags_ , _ulComponentID_ deverá ser 0.</span><span class="sxs-lookup"><span data-stu-id="8829c-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="8829c-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="8829c-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="8829c-118">no Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém as marcas de propriedade que identificam as propriedades passadas no parâmetro _lpCustomProps_ .</span><span class="sxs-lookup"><span data-stu-id="8829c-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="8829c-119">Deve haver uma correspondência de um para um entre cada valor de propriedade no _lpCustomProps_ e uma marca de propriedade no parâmetro _lpCustomPropList_ .</span><span class="sxs-lookup"><span data-stu-id="8829c-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="8829c-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="8829c-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="8829c-121">no Um ponteiro para uma estrutura [SPropValue](spropvalue.md) que contém valores de propriedade para as propriedades a serem codificadas.</span><span class="sxs-lookup"><span data-stu-id="8829c-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="8829c-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="8829c-122">_lpPropList_</span></span>
  
> <span data-ttu-id="8829c-123">no Um ponteiro para uma estrutura **SPropTagArray** que contém as marcas de propriedade para as propriedades a serem codificadas.</span><span class="sxs-lookup"><span data-stu-id="8829c-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="8829c-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="8829c-124">_lppProblems_</span></span>
  
> <span data-ttu-id="8829c-125">bota Um ponteiro para um ponteiro para uma estrutura [STnefProblemArray](stnefproblemarray.md) retornada.</span><span class="sxs-lookup"><span data-stu-id="8829c-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="8829c-126">A estrutura **STnefProblemArray** indica quais propriedades, se houver, não foram codificadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="8829c-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="8829c-127">Se NULL for passado no parâmetro _lppProblems_ , nenhuma matriz de problemas de propriedade será retornada.</span><span class="sxs-lookup"><span data-stu-id="8829c-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8829c-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8829c-128">Return value</span></span>

<span data-ttu-id="8829c-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="8829c-129">S_OK</span></span> 
  
> <span data-ttu-id="8829c-130">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="8829c-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8829c-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="8829c-131">Remarks</span></span>

<span data-ttu-id="8829c-132">Provedores de transporte, provedores de repositórios de mensagens e gateways chamam o método **ITnef:: FinishComponent** para executar o processamento TNEF para um componente, uma mensagem ou um anexo, conforme indicado pelo sinalizador definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="8829c-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="8829c-133">Para que o processamento de componentes seja habilitado, o provedor de chamadas ou o gateway passe o sinalizador TNEF_COMPONENT_ENCODING no _parâmetroulflags_ para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) que abriu o objeto para receber a codificação.</span><span class="sxs-lookup"><span data-stu-id="8829c-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="8829c-134">Passar valores nos parâmetros _lpCustomPropList_ e _lpCustomProps_ executa a codificação de componente equivalente a isso feito pelo método [ITnef::](itnef-setprops.md) SetProps.</span><span class="sxs-lookup"><span data-stu-id="8829c-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="8829c-135">Passar um valor no parâmetro _lpPropList_ realiza a codificação do componente equivalente a feita pelo método [ITnef::](itnef-addprops.md) addprops com o sinalizador TNEF_PROP_INCLUDE definido em _parâmetroulflags_.</span><span class="sxs-lookup"><span data-stu-id="8829c-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="8829c-136">Passar esses valores permite que você execute codificações com uma única chamada em vez de várias chamadas.</span><span class="sxs-lookup"><span data-stu-id="8829c-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="8829c-137">A implementação TNEF relata os problemas de codificação de fluxo TNEF sem interromper o processo **FinishComponent** .</span><span class="sxs-lookup"><span data-stu-id="8829c-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="8829c-138">A estrutura **STnefProblemArray** retornada no _lppProblems_ indica quais atributos TNEF ou propriedades MAPI, se houver, não puderam ser processados.</span><span class="sxs-lookup"><span data-stu-id="8829c-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="8829c-139">O valor retornado no membro **SCODE** de uma das estruturas **STnefProblem** contidas no **STnefProblemArray** indica o problema específico.</span><span class="sxs-lookup"><span data-stu-id="8829c-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="8829c-140">O provedor ou gateway pode funcionar na pressuposição de que todas as propriedades ou atributos para os quais o **FinishComponent** não retorna um relatório de problemas foram processados com êxito.</span><span class="sxs-lookup"><span data-stu-id="8829c-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="8829c-141">Se um provedor ou gateway não funcionar com matrizes problemáticas, ele poderá passar NULL no _lppProblems_; Nesse caso, nenhum conjunto de problemas é retornado.</span><span class="sxs-lookup"><span data-stu-id="8829c-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="8829c-142">O valor retornado em _lppProblems_ é válido somente se a chamada retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="8829c-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="8829c-143">Quando S_OK é retornado, o provedor ou gateway deve verificar os valores retornados na estrutura [STnefProblemArray](stnefproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="8829c-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="8829c-144">Se ocorrer um erro na chamada, a estrutura **STnefProblemArray** não será preenchida e o provedor de chamadas ou o gateway não deverá usar ou liberar a estrutura.</span><span class="sxs-lookup"><span data-stu-id="8829c-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="8829c-145">Se nenhum erro ocorrer na chamada, o provedor de chamada ou o gateway deve liberar a memória para o **STnefProblemArray** chamando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8829c-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8829c-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="8829c-146">See also</span></span>



[<span data-ttu-id="8829c-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="8829c-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="8829c-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="8829c-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="8829c-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8829c-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8829c-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="8829c-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="8829c-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="8829c-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="8829c-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="8829c-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="8829c-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="8829c-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="8829c-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8829c-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

